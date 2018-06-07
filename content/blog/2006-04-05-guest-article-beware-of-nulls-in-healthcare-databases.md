---
title: 'Guest Article: Beware of NULLs in healthcare databases'
author: Shahid N. Shah
type: post
date: 2006-04-05T12:51:30+00:00
url: /2006/04/05/guest-article-beware-of-nulls-in-healthcare-databases/
oc_commit_id:
  - https://www.healthcareguy.com/2006/04/05/guest-article-beware-of-nulls-in-healthcare-databases/1478769026
views:
  - 27995
dsq_thread_id:
  - 44283470
categories:
  - Opinion

---
_Many readers have been asking for more &#8220;practical&#8221; advice on their database models so I&#8217;ve asked a fellow healthcare data architect to lend a hand. [Tom Maloney][1] is a Senior Data Architect for Stockamp and Associates with over 25 years of experience and knowledge working with and designing databases for most industries. Tom has done a lot of freelance contracting through his own company where he lives and breathes data modeling. In this guest article Tom is discussing the pitfalls of allowing NULLs in healthcare databases and his suggestions and arguments have a lot of merit. As usual, recommendations like the ones Tom is making do not apply in all circumstances but they are worth reviewing._<div class=Section1> <p class=MsoNormal>On our patient claim system the hospital wanted to know the average payment amount received between two periods of time. As we all know the average is the sum of the values divided by the number of rows. So we constructed a simple query to calculate the average.</p> <p class=MsoNormal style='text-autospace:none'>

<span style='font-size:10.0pt;
font-family:"Courier New";color:blue'>Select</span> <span style='font-size:10.0pt;
font-family:"Courier New"'></span><span style='color:fuchsia'>SUM</span><span style='color:gray'>(</span>Amount<span style='color:gray'>)/</span><span style='color:fuchsia'>COUNT</span><span style='color:gray'>(*)</span> <span style='color:blue'>FROM</span> [dbo]<span style='color:gray'>.</span>[Payment]</p> <p class=MsoNormal><span style='font-size:10.0pt;font-family:"Courier New";
color:blue'>WHERE</span><span style='font-size:10.0pt;font-family:"Courier New"'><br /> EffectiveDate </span><span style='color:gray'>BETWEEN</span> <span style='color:red'>&#8216;20060330&#8217;</span>
  
<span style='color:gray'>AND</span> <span style='color:red'>&#8216;20060410&#8217;</span></p> <p class=MsoNormal>After the answer was returned; we remembered that SQL
  
provides a function that calculates and returns the average, so we decided to
  
use it. When we ran this query</p> <p class=MsoNormal style='text-autospace:none'><span style='font-size:10.0pt;
font-family:"Courier New";color:blue'>Select</span> <span style='font-size:10.0pt;
font-family:"Courier New"'></span><span style='color:fuchsia'>AVG</span><span style='color:gray'>(</span>Amount<span style='color:gray'>)</span> </p> <p class=MsoNormal style='text-autospace:none'><span style='font-size:10.0pt;
font-family:"Courier New";color:blue'>FROM</span> <span style='font-size:10.0pt;
font-family:"Courier New"'>[dbo]</span><span style='color:gray'>.</span>[Payment]</p> <p class=MsoNormal style='text-autospace:none'><span style='font-size:10.0pt;
font-family:"Courier New";color:blue'>WHERE</span> <span style='font-size:10.0pt;
font-family:"Courier New"'>EffectiveDate </span><span style='color:gray'>BETWEEN</span>
  
<span style='color:red'>&#8216;20060330&#8217;</span> <span style='color:gray'>AND</span> <span style='color:red'>&#8216;20060410&#8217;</span></p> <p class=MsoNormal>we had a completely different answer. Which one was correct or could they both be wrong? What cause the difference? The culprit turned out to be NULL values in some of the columns. </p> <p class=MsoNormal>To prove this we performed a little experiment by creation and population the following table called Payment populated it with ten rows. We allowed some of the column in a few rows to contain NULL values (Note: the syntax is Transact-SQL from Microsoft SQL Server).</p> <p class=MsoNormal> Table Creation:</p> <p class=MsoNormal style='text-autospace:none'><span style='font-size:10.0pt;
font-family:"Courier New";color:blue'>CREATE</span> <span style='font-size:10.0pt;
font-family:"Courier New"'></span><span style='color:blue'>TABLE</span> [dbo]<span style='color:gray'>.</span>[Payment]<span style='color:gray'>(</span></p> <p class=MsoNormal style='text-autospace:none'>      <span style='font-size:10.0pt;
font-family:"Courier New"'>[Payment_Key] [int] </span><span style='color:gray'>NOT</span>
  
<span style='color:gray'>NULL,</span></p> <p class=MsoNormal style='text-autospace:none'>      <span style='font-size:10.0pt;
font-family:"Courier New"'>[Amount] [money] </span><span style='color:gray'>NULL,</span></p> <p class=MsoNormal style='text-autospace:none'>      <span style='font-size:10.0pt;
font-family:"Courier New"'>[EffectiveDate] [datetime] </span><span style='color:gray'>NULL,</span></p> <p class=MsoNormal style='text-autospace:none'>      <span style='font-size:10.0pt;
font-family:"Courier New"'>[Note] [varchar]</span><span style='color:gray'>(</span>1024<span style='color:gray'>)</span> <span style='color:gray'>NOT</span> <span style='color:gray'>NULL</span> <span style='color:blue'>DEFAULT</span> <span style='color:gray'>(</span><span style='color:red'>&#8221;</span><span style='color:gray'>),</span></p> <p class=MsoNormal style='text-autospace:none'>      <span style='font-size:10.0pt;
font-family:"Courier New"'>[PaymentRefNumber] [varchar]</span><span style='color:gray'>(</span>16<span style='color:gray'>)</span> <span style='color:gray'>NOT</span> <span style='color:gray'>NULL,</span></p> <p class=MsoNormal style='text-autospace:none'><span style='font-size:10.0pt;
font-family:"Courier New";color:blue'>PRIMARY</span> <span style='font-size:
10.0pt;font-family:"Courier New"'></span><span style='color:blue'>KEY</span> <span style='color:blue'>CLUSTERED</span> </p> <p class=MsoNormal style='text-autospace:none'><span style='font-size:10.0pt;
font-family:"Courier New";color:gray'>(</span></p> <p class=MsoNormal style='text-autospace:none'>      <span style='font-size:10.0pt;
font-family:"Courier New"'>[Payment_Key] </span><span style='color:blue'>ASC</span></p> <p class=MsoNormal style='text-autospace:none'><span style='font-size:10.0pt;
font-family:"Courier New";color:gray'>)</span><span style='font-size:10.0pt;
font-family:"Courier New";color:blue'>WITH</span> <span style='font-size:10.0pt;
font-family:"Courier New"'></span><span style='color:gray'>(</span>IGNORE\_DUP\_KEY <span style='color:gray'>=</span> <span style='color:blue'>OFF</span><span style='color:gray'>)</span></p> <p class=MsoNormal style='text-autospace:none'><span style='font-size:10.0pt;
font-family:"Courier New";color:gray'>)</span></p> <p class=MsoNormal>Go</p> <p class=MsoNormal>Populate the Table:</p> <p class=MsoNormal style='text-autospace:none'><span style='font-size:10.0pt;
font-family:"Courier New";color:blue'>INSERT</span> <span style='font-size:10.0pt;
font-family:"Courier New"'></span><span style='color:blue'>INTO</span> [dbo]<span style='color:gray'>.</span>[Payment]</p> <p class=MsoNormal style='text-autospace:none'><span style='font-size:10.0pt;
font-family:"Courier New";color:blue'>VALUES</span> <span style='font-size:10.0pt;
font-family:"Courier New"'></span><span style='color:gray'>(</span>1<span style='color:gray'>,</span> $125.00<span style='color:gray'>,</span> <span style='color:gray'>NULL,</span> <span style='color:red'>&#8216;Payment 1&#8217;</span><span style='color:gray'>,</span> <span style='color:red'>&#8216;1&#8217;</span><span style='color:gray'>) &#8212;</span><span style='font-size:10.0pt;
font-family:Wingdings;color:gray'>ß</span> <span style='font-size:10.0pt;
font-family:"Courier New";color:gray'>Null in date </span></p> <p class=MsoNormal style='text-autospace:none'><span style='font-size:10.0pt;
font-family:"Courier New";color:blue'>INSERT</span> <span style='font-size:10.0pt;
font-family:"Courier New"'></span><span style='color:blue'>INTO</span> [dbo]<span style='color:gray'>.</span>[Payment]</p> <p class=MsoNormal style='text-autospace:none'><span style='font-size:10.0pt;
font-family:"Courier New";color:blue'>VALUES</span> <span style='font-size:10.0pt;
font-family:"Courier New"'></span><span style='color:gray'>(</span>2<span style='color:gray'>,</span> $125.00<span style='color:gray'>,</span> <span style='color:red'>&#8216;20060403&#8217;</span><span style='color:gray'>,</span> <span style='color:red'>&#8216;Payment 2&#8217;</span><span style='color:gray'>,</span> <span style='color:red'>&#8216;2&#8217;</span><span style='color:gray'>)</span></p> <p class=MsoNormal style='text-autospace:none'><span style='font-size:10.0pt;
font-family:"Courier New";color:blue'>INSERT</span> <span style='font-size:10.0pt;
font-family:"Courier New"'></span><span style='color:blue'>INTO</span> [dbo]<span style='color:gray'>.</span>[Payment]</p> <p class=MsoNormal style='text-autospace:none'><span style='font-size:10.0pt;
font-family:"Courier New";color:blue'>VALUES</span> <span style='font-size:10.0pt;
font-family:"Courier New"'></span><span style='color:gray'>(</span>3<span style='color:gray'>,</span> <span style='color:gray'>Null,</span> <span style='color:red'>&#8216;20060404&#8217;</span><span style='color:gray'>,</span> <span style='color:red'>&#8216;Payment 3&#8217;</span><span style='color:gray'>,</span> <span style='color:red'>&#8216;3&#8217;</span><span style='color:gray'>) &#8212;</span><span style='font-size:10.0pt;font-family:Wingdings;color:gray'>ß</span> <span style='font-size:10.0pt;font-family:"Courier New";color:gray'>Null in Amount</span></p> <p class=MsoNormal style='text-autospace:none'><span style='font-size:10.0pt;
font-family:"Courier New";color:blue'>INSERT</span> <span style='font-size:10.0pt;
font-family:"Courier New"'></span><span style='color:blue'>INTO</span> [dbo]<span style='color:gray'>.</span>[Payment]</p> <p class=MsoNormal style='text-autospace:none'><span style='font-size:10.0pt;
font-family:"Courier New";color:blue'>VALUES</span> <span style='font-size:10.0pt;
font-family:"Courier New"'></span><span style='color:gray'>(</span>4<span style='color:gray'>,</span> $125.00<span style='color:gray'>,</span> <span style='color:red'>&#8216;20060404&#8217;</span><span style='color:gray'>,</span> <span style='color:red'>&#8216;Payment 4&#8217;</span><span style='color:gray'>,</span> <span style='color:red'>&#8216;4&#8217;</span><span style='color:gray'>)</span></p> <p class=MsoNormal style='text-autospace:none'><span style='font-size:10.0pt;
font-family:"Courier New";color:blue'>INSERT</span> <span style='font-size:10.0pt;
font-family:"Courier New"'></span><span style='color:blue'>INTO</span> [dbo]<span style='color:gray'>.</span>[Payment]</p> <p class=MsoNormal style='text-autospace:none'><span style='font-size:10.0pt;
font-family:"Courier New";color:blue'>VALUES</span> <span style='font-size:10.0pt;
font-family:"Courier New"'></span><span style='color:gray'>(</span>5<span style='color:gray'>,</span> $125.00<span style='color:gray'>,</span> <span style='color:red'>&#8216;20060405&#8217;</span><span style='color:gray'>,</span> <span style='color:red'>&#8216;Payment 5&#8217;</span><span style='color:gray'>,</span> <span style='color:red'>&#8216;5&#8217;</span><span style='color:gray'>)</span></p> <p class=MsoNormal style='text-autospace:none'><span style='font-size:10.0pt;
font-family:"Courier New";color:blue'>INSERT</span> <span style='font-size:10.0pt;
font-family:"Courier New"'></span><span style='color:blue'>INTO</span> [dbo]<span style='color:gray'>.</span>[Payment]</p> <p class=MsoNormal style='text-autospace:none'><span style='font-size:10.0pt;
font-family:"Courier New";color:blue'>VALUES</span> <span style='font-size:10.0pt;
font-family:"Courier New"'></span><span style='color:gray'>(</span>6<span style='color:gray'>,</span> $125.00<span style='color:gray'>,</span> <span style='color:red'>&#8216;20060405&#8217;</span><span style='color:gray'>,</span> <span style='color:red'>&#8216;Payment 6&#8217;</span><span style='color:gray'>,</span> <span style='color:red'>&#8216;6&#8217;</span><span style='color:gray'>)</span></p> <p class=MsoNormal style='text-autospace:none'><span style='font-size:10.0pt;
font-family:"Courier New";color:blue'>INSERT</span> <span style='font-size:10.0pt;
font-family:"Courier New"'></span><span style='color:blue'>INTO</span> [dbo]<span style='color:gray'>.</span>[Payment]</p> <p class=MsoNormal style='text-autospace:none'><span style='font-size:10.0pt;
font-family:"Courier New";color:blue'>VALUES</span> <span style='font-size:10.0pt;
font-family:"Courier New"'></span><span style='color:gray'>(</span>7<span style='color:gray'>,</span> <span style='color:gray'>NULL,</span> <span style='color:gray'>NULL,</span> <span style='color:red'>&#8216;Payment 7&#8217;</span><span style='color:gray'>,</span> <span style='color:red'>&#8216;7&#8217;</span><span style='color:gray'>) &#8212;</span><span style='font-size:10.0pt;font-family:
Wingdings;color:gray'>ß</span> <span style='font-size:10.0pt;font-family:"Courier New";
color:gray'>Null Amount and date</span></p> <p class=MsoNormal style='text-autospace:none'><span style='font-size:10.0pt;
font-family:"Courier New";color:blue'>INSERT</span> <span style='font-size:10.0pt;
font-family:"Courier New"'></span><span style='color:blue'>INTO</span> [dbo]<span style='color:gray'>.</span>[Payment]</p> <p class=MsoNormal style='text-autospace:none'><span style='font-size:10.0pt;
font-family:"Courier New";color:blue'>VALUES</span> <span style='font-size:10.0pt;
font-family:"Courier New"'></span><span style='color:gray'>(</span>8<span style='color:gray'>,</span> $125.00<span style='color:gray'>,</span> <span style='color:red'>&#8216;20060406&#8217;</span><span style='color:gray'>,</span> <span style='color:red'>&#8216;Payment 8&#8217;</span><span style='color:gray'>,</span> <span style='color:red'>&#8216;8&#8217;</span><span style='color:gray'>)</span></p> <p class=MsoNormal style='text-autospace:none'><span style='font-size:10.0pt;
font-family:"Courier New";color:blue'>INSERT</span> <span style='font-size:10.0pt;
font-family:"Courier New"'></span><span style='color:blue'>INTO</span> [dbo]<span style='color:gray'>.</span>[Payment]</p> <p class=MsoNormal style='text-autospace:none'><span style='font-size:10.0pt;
font-family:"Courier New";color:blue'>VALUES</span> <span style='font-size:10.0pt;
font-family:"Courier New"'></span><span style='color:gray'>(</span>9<span style='color:gray'>,</span> $125.00<span style='color:gray'>,</span> <span style='color:gray'>NULL,</span> <span style='color:red'>&#8216;Payment 9&#8217;</span><span style='color:gray'>,</span> <span style='color:red'>&#8216;9&#8217;</span><span style='color:gray'>) &#8212;</span><span style='font-size:10.0pt;
font-family:Wingdings;color:gray'>ß</span> <span style='font-size:10.0pt;
font-family:"Courier New";color:gray'>Null date</span></p> <p class=MsoNormal style='text-autospace:none'><span style='font-size:10.0pt;
font-family:"Courier New";color:blue'>INSERT</span> <span style='font-size:10.0pt;
font-family:"Courier New"'></span><span style='color:blue'>INTO</span> [dbo]<span style='color:gray'>.</span>[Payment]</p> <p class=MsoNormal style='text-autospace:none'><span style='font-size:10.0pt;
font-family:"Courier New";color:blue'>VALUES</span> <span style='font-size:10.0pt;
font-family:"Courier New"'></span><span style='color:gray'>(</span>10<span style='color:gray'>,</span> $125.00<span style='color:gray'>,</span> <span style='color:red'>&#8216;20060407&#8217;</span><span style='color:gray'>,</span> <span style='color:red'>&#8216;Payment 10&#8217;</span><span style='color:gray'>,</span> <span style='color:red'>&#8217;10&#8217;</span><span style='color:gray'>)</span></p> <p class=MsoNormal>GO</p> 

If you add all of the values in the Amount column we have $1000.00, there are ten rows, so the average should be $100.00, right? Not really. We were only looking for rows between Mar 30 and Apr 10, 2006. A NULL can represent any value, it is unknown at this time, and we do not know if NULL means not entered or if it is a place holder for valid date within the range we are interested in.

As we will find out a little later SQL counts NULL sometime and other times it ignores it. Using the BETWEEN predicate SQL ignores NULLs. This gives us actually seven rows to divide into the sum of the amount. Also, one of the rows with a valid date range contains a NULL amount giving us only six Amounts to sum (both the SUM and AVG SQL function ignores NULLs), giving a total amount of $750.00, divided by seven rows we have an average of $107.14 rounded). Not $1000.00 divided by 10 rows yielding $100.00 average.<p class=MsoNormal style='text-autospace:none'>

<span style='font-size:10.0pt;
font-family:"Courier New";color:blue'>Select</span> <span style='font-size:10.0pt;
font-family:"Courier New"'></span><span style='color:fuchsia'>SUM</span><span style='color:gray'>(</span>Amount<span style='color:gray'>)/</span><span style='color:fuchsia'>COUNT</span><span style='color:gray'>(*)</span> <span style='color:blue'>FROM</span> [dbo]<span style='color:gray'>.</span>[Payment]</p> <p class=MsoNormal><span style='font-size:10.0pt;font-family:"Courier New";
color:blue'>WHERE</span><span style='font-size:10.0pt;font-family:"Courier New"'><br /> EffectiveDate </span><span style='color:gray'>BETWEEN</span> <span style='color:red'>&#8216;20060330&#8217;</span>
  
<span style='color:gray'>AND</span> <span style='color:red'>&#8216;20060410&#8217;</span></p> 

The result is **$107.1428**, this is the answer we were looking for. Let’s try using the AVG function and see what is returned:<p class=MsoNormal style='text-autospace:none'>

<span style='font-size:10.0pt;
font-family:"Courier New";color:blue'>&nbsp;</span></p> <p class=MsoNormal style='text-autospace:none'><span style='font-size:10.0pt;
font-family:"Courier New";color:blue'>Select</span> <span style='font-size:10.0pt;
font-family:"Courier New"'></span><span style='color:fuchsia'>AVG</span><span style='color:gray'>(</span>Amount<span style='color:gray'>)</span> </p> <p class=MsoNormal style='text-autospace:none'><span style='font-size:10.0pt;
font-family:"Courier New";color:blue'>FROM</span> <span style='font-size:10.0pt;
font-family:"Courier New"'>[dbo]</span><span style='color:gray'>.</span>[Payment]</p> <p class=MsoNormal style='text-autospace:none'><span style='font-size:10.0pt;
font-family:"Courier New";color:blue'>WHERE</span> <span style='font-size:10.0pt;
font-family:"Courier New"'>EffectiveDate </span><span style='color:gray'>BETWEEN</span>
  
<span style='color:red'>&#8216;20060330&#8217;</span> <span style='color:gray'>AND</span> <span style='color:red'>&#8216;20060410&#8217;</span></p> 

This time for the same set of data we got **$125.00** as an average. What’s going on here? The answer lies in how SQL treats NULLs.

The following provides a deeper look into how SQL handled NULLs.

Other that the special way the SQL Server has to store a null and the extra logic SQL Server has to do to identify a column containing a null, here are a few favorites (comments from C. J. Date<a href="#_ftn1" name="_ftnref1" title=""><span class=MsoFootnoteReference></span><span class=MsoFootnoteReference></span><span style='font-size:12.0pt;font-family:"Times New Roman"'>[1]</span></a>):

<li class=MsoNormal>To test in a WHERE clause whether a field is null, SQL provides the special comparison “field IS NULL.” It is not intuitively obvious why the user has to write “field IS NULL” and not “field = NULL” – especially as the system “field = NULL” is used in the SET clause of the UPDATE statement (and the SET assignment process) to update a field to the null value. (In fact, the WHERE clause “WHERE field = NULL” is syntactically illegal – SQL Server’s syntax does allow it (some vendors do provide a SET statement to allow this).</li> <li class=MsoNormal>SQL92 has solved the problem of comparing NULLs by adding a new predicate of the form <search condition> IS [NOT] TRUE | FALSE | UNKNOWN, which will let you map any combination of three-value logic to two-value logic. For example, ((Age < 18) AND (Gender = ‘F’)) IS NOT FALSE will return TRUE if (Age IS NULL) or (Gender IS NULL) and the remaining condition is not NULL.</li> <li class=MsoNormal>NULL values are considered as duplicates of each other for the purpose on UNIQUE and DISTINCT and ORDER BY but not for the purpose of WHERE and GROUP BY. NULL values are also considered as greater than all non-null values for the purpose of ORDER BY but not for the purposes of WHERE.</li> <li class=MsoNormal>NULL values are always eliminated from the argument to a built-in function such as SUM or AVG, regardless of whether DISTINCT is specified in the function reference – except for the case of COUNT(*), which counts all rows, including duplicates and including all-null rows. Thus for example, given:</li> <p class=MsoNormal style='margin-left:.5in'>SELECT AVG(Status) FROM S &#8212;


  
Result: x</p> <p class=MsoNormal style='margin-left:.5in'>SELECT SUM(Status) FROM S &#8212;
  
Result: y</p> <p class=MsoNormal style='margin-left:.5in'>SELECT COUNT(*) FROM S &#8212;
  
Result: z</p> <p class=MsoNormal style='margin-left:.5in'> there is no guarantee that x = y/z</p> <ol style='margin-top:0in' start=5 type=1> <li class=MsoNormal>Likewise, the function reference SUM (F) is _not_ semantically equivalent to the expression: f1 + f2 + … + fn where f1, f2…, fn are the values appearing in field F at the time the function is evaluated. Perhaps, even more counter-intuitively, the expression </li> </ol> <p class=MsoNormal style='margin-left:.5in'>SUM (F1 + F2)</p> <p class=MsoNormal style='margin-left:.5in'>Is not equivalent to the expression</p> <p class=MsoNormal style='margin-left:.5in'>SUM (F1) + SUM (F2)</p> <ol style='margin-top:0in' start=6 type=1> <li class=MsoNormal>Since by definition NULL represents an unknown value, we define the results in every case to be _unknown_ (i.e., NULL) also, rather than _true_ or _false_. To deal with NULL values properly, therefore, it is necessary to adopt 3-valued logic in place of the usual 2-valued logic. The 3-valued logic is defined by the truth tables shown below. Note that _unknown_ or null truth-value can reasonably be interpreted as “maybe.”</li> </ol> <p class=MsoNormal style='margin-left:1.0in'><u>AND T ? F</u> <u>OR
  
T ? F</u> <u>NOT </u></p> <p class=MsoNormal style='margin-left:1.0in'> <span lang=DE>T T ? F
  
T T T T T F</span></p> <p class=MsoNormal style='margin-left:1.0in'><span lang=DE> ? ? ? F
  
? </span>T ? ? ? ?</p> <p class=MsoNormal style='margin-left:1.0in'> F F F F F
  
T ? F F T</p> <ol style='margin-top:0in' start=7 type=1> <li class=MsoNormal>Consider the question of whether set are allowed to contain NULL values. Suppose, for example, that the collection C = {1, 2, 3, ?} is to be permitted as a legal set. There are two possibilities.</li> </ol> <ol style='margin-top:0in' start=1 type=a> <li class=MsoNormal>The particular null value appears in C is of course unknown, but is known to be distinct from 1, 2, and 3.</li> <li class=MsoNormal>The NULL value in C is completely unknown (i.e., it may in fact stand for one of the values 1, 2, 3), in which case the cardinality of C in turn is unknown (it may be either 3 or 4).</li> </ol> <li class=MsoNormal>Using the BETWEEN predicate with NULL values. The result of this predicate with NULL values for <value expression>, <low value expression>, or <high value expression> follow directly from definition. If both <low value expression> and <high value expression> are NULL, the result is _unknown_ for any value of <value expression>. If <low value expression> or <high value expression> is NULL, but not both, the results is determined by the value of <value expression> and its comparison with the remaining non-NULL term. If <value expression> is NULL the results are _unknown_ for any values of <low value expression> and <high value expression>.</li> <li class=MsoNormal>Host languages have to handle NULLs in non-standard ways. The programmer should know how NULLs are handled when they are passed to the host language. No standard host language for which embeddings are defined support NULLs, which is another good reason to avoid using them in database schemas.</li> <p class=MsoNormal>On the whole I set all data type not to allow NULLs and provide default values when the column is not required. But what about dates and Boolean value columns where the data is not know at time of entry? There are times in designing a healthcare database schema where NULLs values may be allowed, these columns needs to be handled on an exception basis and rather than the norm. Usually I find a workaround, for example, if a Patient’s Gender is not always known at the time of entry, instead of using a Boolean, use a single character to hold a code (F=Female, M=Male, O=Other, U=Unknown, A=Ambiguous, N=Not applicable).</p> <p class=MsoNormal>Another example is for dates. If a date is not known at time of entry I provide a default. Most dates record an event in time or a date range (Begin and End dates). For dates that represent a date in time I choose a low (e.g., 01/01/1900) or high (e.g., 11/27/4637) default date depending on the how the column would be used in a query. If developers or anyone else want to see a NULL value returned, I create a view over the table that contains a NULLIF<a href="#_ftn2" name="_ftnref2" title=""><span class=MsoFootnoteReference></span><span class=MsoFootnoteReference></span><span style='font-size:12.0pt;font-family:"Times New Roman"'>[2]</span></a> returning a NULL (e.g., NULLIF(MyDate, 19000101). Columns that represent a date range I default the From Date with 01/01/1900 and the Thru Date with 46371127. </p> <p class=MsoNormal>When my queries are ran against range date with defaults I get the behavior I expect. When the range date columns contain NULLs the result are not what is expected or I have to write special SQL to handle it. In the example, by changing the table to not allow NULLs and replacing unknown dates with 19000101 and unknown Amounts with $0.00, both AVG and SUM(Amount)/Count(*) returns the same value.</p> <p class=MsoNormal>All Character and Variable-Character data types I default with an empty string. When the column is selected, it is displayed with as an invisible value. By using NOT NULL data types you are assured that the results returned will be as you expect without having to handle NULLs differently. In addition, some vendor database’s performance improves because columns that allow NULLs must be evaluated differently for comparisons. If Nulls are used try and minimize it use.</p> </div> 

<div>
  <br clear=all/></p> <hr align=left size=1 width="33%"/> <div id=ftn1> <p class=MsoFootnoteText><a href="#_ftnref1" name="_ftn1" title=""><span class=MsoFootnoteReference></span><span class=MsoFootnoteReference></span><span style='font-size:10.0pt;font-family:"Times New Roman"'>[1]</span></a><br /> Relational Database, Selected Writings, CJ Date, .Addison Weisley</p>
</div><div id=ftn2> <p class=MsoFootnoteText>

<a href="#_ftnref2" name="_ftn2" title=""><span class=MsoFootnoteReference></span><span class=MsoFootnoteReference></span><span style='font-size:10.0pt;font-family:"Times New Roman"'>[2]</span></a>
  
Microsoft SQL Server T-SQL </p> </div> </div>

 [1]: tmaloney1@west-connect.com