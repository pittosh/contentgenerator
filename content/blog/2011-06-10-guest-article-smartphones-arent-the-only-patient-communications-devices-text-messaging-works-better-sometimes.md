---
title: 'Guest Article: Smartphones aren’t the only patient communications devices, text messaging works better sometimes'
author: Shahid N. Shah
type: post
date: 2011-06-11T01:02:42+00:00
url: /2011/06/10/guest-article-smartphones-arent-the-only-patient-communications-devices-text-messaging-works-better-sometimes/
oc_commit_id:
  - https://www.healthcareguy.com/2011/06/10/guest-article-smartphones-arent-the-only-patient-communications-devices-text-messaging-works-better-sometimes/1478770742
dsq_thread_id:
  - 328256202
categories:
  - Uncategorized

---
_With the mobile and tablet frenzy at a fevered pitch, most of us technical folks end up thinking that the best way to reach patients is through the most expensive means possible (a high end PC, a tablet, a smart phone, etc.) because those are the devices we&#8217;re using all the time, too. However, sometimes (maybe more often than not), simple text messaging to feature phones and smart phones may be the best option. I don&#8217;t think that personalizing healthcare always need expensive devices so I reached out to Cliff Haas, Sr. Director of Connectivity and Partner Management North America at [Clickatell][1], to &#8220;talk tech&#8221; about how personalized mobile messaging can become a new horizon in healthcare and show us how it&#8217;s done (including some sample code). Here&#8217;s what Cliff shared:_

Personalized text messaging in healthcare is the new antidote to healthcare costs, patient waiting times and patient’s general health maintenance, according to a study by PricewaterhouseCoopers’ Health Research Institute.

The reasons for the success of this new communication medium are clear. Statistics show that a staggering 71% of the global population or 5.3 billion people own a mobile handset\*, in contrast, only 2 billion people are connected to the Internet\**.  The store and forward nature of messaging makes this medium more convenient than a voice call and it is also far less intrusive than having to accept or return a phone cal. This convenience gives patients the ability to read messages in privacy at a suitable time.

**Benefits for all**

Perhaps the greatest advantage to implementing an SMS-based solution in healthcare is that the benefits are realized by both the patient as well as the health care provider.

**Healthcare Provider**

Healthcare providers have a need to keep their overheads low while maintaining exceptionally high standards in the service they provide. This is not an easy task in any environment. If we look at the effort it takes for a medical group to manage a schedule of daily appointments, the cost can be considerable. The salary for a Medical Receptionist is approximately $30,000.00 annually. The responsibilities for the position are broad. A quick internet search shows the following:

> [**Medical Secretaries**][2] ****
> 
> Perform secretarial duties utilizing specific knowledge of medical terminology and hospital, clinic, or laboratory procedures. Duties include scheduling appointments, billing patients, and compiling and recording medical charts, reports, and correspondence.
> 
> [**Front Desk/Receptionists, Medical or Dental Office**][3] ****
> 
> Answer phones in a medical / dental office. Schedule appointments and maintain schedule book. Take payments and co-payments from patients. Collect insurance information.” (www.payscale.com)

Now consider how a well implemented messaging integration platform could provide an automated solution to many of these functions, which in turn frees the healthcare professional to tend to other responsibilities.  Messages could be used to:

  * Send reminders to patients, advising of their forthcoming appointments
  * Accept responses to verify the patients availability
  * Send  reminders to bring updated insurance information
  * Send billing reminders
  * Send follow-up messages to assure customer satisfaction
  * Notify or remind patient of health care regiment protocol or protocol changes.
  * Notify the availability of test results

**Patient**

The patient expects to receive top-grade service from their healthcare provider. In part, this means receiving timely information while avoiding being a nuisance, not an easy task. Patients receiving messages as stated above are able to effectively communicate with their healthcare provider in a far less intrusive manner than a voice call and can do so while maintaining their busy lifestyle.

**Making it work isn’t brain surgery**

Fortunately, SMS integration into the healthcare providers practice can be very easy. If you have the flexibility to try a new application in your office, you could reach out to an SMS solution provider such as Clickatell for guidance on where to find the best application for your requirements.

Alternatively you might have a CRM or scheduling application that is deeply embedded within your business. In this case you can take advantage of the API sets made available to developers. Clickatell and similar vendors offer a wide variety of API types and XML would be a great candidate for this use.See how messaging works &#8211; click the picture below for a larger version:

[<img src="/img/uploads/2011/06/clickatell_guest_article_01-300x195.png" alt="" title="clickatell_guest_article_01" width="300" height="195" class="aligncenter size-medium wp-image-1205" />][4]

If you decide you are going to integrate at an API level, you will need to have an account with a provider such as Clickatell. Once you have that account you will use the assigned credentials to populate an XML over HTTP Post through your application.

<pre>&lt;clickAPI&gt;
    &lt;sendMsg&gt;
        &lt;api_id&gt;1&lt;/api_id&gt;
        &lt;user&gt;demo&lt;/user&gt;
        &lt;password&gt;demo&lt;/password&gt;
        &lt;to&gt;123456567890123&lt;/to&gt;
        &lt;text&gt;Initial text message&lt;/text&gt;
        &lt;from&gt;me&lt;/from&gt;
    &lt;/sendMsg&gt;
&lt;/clickAPI&gt;
</pre>

For the sake of this example, you may have a client for scheduling or CRM built on Microsoft Access. This allows HTTP posting of the XML formatted data from the application. 

<pre>Public Function fcSend(strRequestXML As String)
    Dim objXMLHttp, sResponse
    Set objXMLHttp = CreateObject("MSXML2.ServerXMLHTTP")

    objXMLHttp.Open "POST", strAPIUrl, False
    objXMLHttp.setRequestHeader "Content-Type", "application/x-www-form-urlencoded"
    objXMLHttp.send ("qf=xml&xml=" & URLEncode(strRequestXML))

    If objXMLHttp.Status = 200 Then
         sResponse = objXMLHttp.responseText
    End If
    
    Set objXMLHttp = Nothing
    fcSend = sResponse

End Function

Function URLEncode(strData)
  Dim I, strTemp, strChar, strOut, intAsc
  
    strTemp = Trim(strData)
  
    For I = 1 To Len(strTemp)
        strChar = Mid(strTemp, I, 1)
        intAsc = Asc(strChar)
        If (intAsc >= 48 And intAsc &lt;= 57) Or (intAsc >= 97 And intAsc &lt;= 122) Or (intAsc >= 65 And intAsc &lt;= 90) Then
            strOut = strOut &#038; strChar
        Else
            strOut = strOut &#038; "%" &#038; Hex(intAsc)
        End If
    Next
  
URLEncode = strOut
  
End Function
</pre>

**Your next step**

These are just examples of how SMS messaging can be used to provide the Healthcare industry with an easy-to-use solution to common business demands. You can find additional use case examples, supporting statistics and technical guidance at www.clickatell.com or ask questions as comments below.

 [1]: http://www.clickatell.com
 [2]: http://www.payscale.com/Job_Description/Medical_Secretaries
 [3]: http://www.payscale.com/Job_Description/Front_Desk%2fReceptionists%2c_Medical_or_Dental_Office
 [4]: /img/uploads/2011/06/clickatell_guest_article_01.png