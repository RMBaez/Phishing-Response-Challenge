<img width="570" alt="image" src="https://github.com/RMBaez/Phishing-Response-Challenge/assets/170957530/5e9a6d57-e989-42a8-a440-f2a044dd838b">


<h1> Phishing Response Challenge </h1>
This tutorial outlines the identification of phishing emails and manually triage them to report on their intent and collect valuable data.
<br />



<h2>Environments and Technologies Used</h2>

- Thunderbird
- Sublime 3
- Whois.domaintools.com



<h2>Deployment and Configuration Steps</h2>

- Question 1: Which of the 5 emails have you identified as being malicious?
- Question 2: First Malicious Email: What is the sending address?
- Question 3: First Malicious Email: What is the subject line?
- Question 4: First Malicious Email: Who are the recipients?
- Question 5: First Malicious Email: What is the Reply-to address? (If not present, write "none")
- Question 6: First Malicious Email: What is the date and time the email was sent?
- Question 7: First Malicious Email: What is the sending server IP?
- Question 8: First Malicious Email: What is the reverse DNS hostname of the sending server IP?
- Question 9: First Malicious Email: What is the full URL?
- Question 10: Second Malicious Email: What is the sending address?
- Question 11: Second Malicious Email: What is the subject line?
- Question 12: Second Malicious Email: Who are the recipients?
- Question 13: Second Malicious Email: What is the Reply-to address? (If not present, write "none")
- Question 14: Second Malicious Email: What is the date and time the email was sent?
- Question 15: Second Malicious Email: What is the sending server IP?
- Question 16: Second Malicious Email:  What is the reverse DNS hostname of the sending IP?
- Question 17: Second Malicious Email: What is the file name, including extension?
- Question 18: Second Malicious Email: What is the SHA256 hash value of the file?


<h2>Deployment and Configuration Steps</h2>


<p>
Question 1: Which of the 5 emails have you identified as being malicious?
</p>
<br />


<p> Email 1 </p>

<p>
<img width="569" alt="image" src="https://github.com/RMBaez/Phishing-Response-Challenge/assets/170957530/bfed199c-4b3d-4b17-9cf5-9b8d895fca00">
</p>

<p>
It is immediately clear that this email is highly suspicious:

The sending address is set as ‘auto-confirm.info-amazon.co.uk (where info-amazon.co.uk is the domain, not amazon.co.uk), but we can see it’s actually coming from QPE77756@mun.ca. This definitely isn't Amazon
Formating/styling is inconsistent - emails from huge brands such as Amazon are styled well, and do not use varying fonts
- The email is not addressed to a specific person which is often seen in legitimate emails, instead it is addressed to a generic recipient ‘Amazon user’
- The email features poor and incorrect grammar such as ‘Your ID’ (should be your account), and ‘From Amazon Store’
- Has an obvious call-to-action button, enticing the user to click on the link for the ‘Help Page - Refund Form’ (emails do use legitimate call-to-actions, but this is also a part of phishing with URLs)
  
We've found our first malicious phishing email.
</p>
<br />


<p> Email 2 </p>

<p> <img width="569" alt="image" src="https://github.com/RMBaez/Phishing-Response-Challenge/assets/170957530/ca5753d5-0bf5-4bce-b8d1-c20732f5768f"> </p>

<p> 
- Email is spam-themed, trying to convince non-technical users that they are going to get a portion of someone's lottery winnings
- The email is not addressed directly to the recipient, suggesting it is being mass-mailed to a large list of people
- There is a URL in the body, however it is not hyperlinked. A quick Google search tells us that ‘thescottishsun[.]co[.]uk’ is a legitimate news site, and is not malicious
- The email provides an email address to contact that is different from the sender
  
Based on this information, this email is not malicious. It should be classed as spam/scam as it is trying to convince recipients to send personal details to a Gmail address, using the story behind a legitimate news article regarding lottery winners in Scotland.
</p>


<p> Email 3 </p>

<p>
<img width="552" alt="image" src="https://github.com/RMBaez/Phishing-Response-Challenge/assets/170957530/14d5e5ba-60db-4893-a931-2ebe0cbe96c5">
</p>

<p> 
- The sender is a Gmail address, despite the email claiming to be from the UK's National Health Service
- The image used in the email is a generic stock image and doesn't show any NHS or UK Government branding to match the theme of the email
- The email is addressed to a generic recipient ‘Sir/Madam’
- The email is telling the recipient to open the attached file (call-to-action)
- A sense of urgency is created to generate an emotional response using the sentence ‘If you do not act soon, we will give your slot to someone else’ - this is trying to make people act quicker than they can think
- The attachment is named ‘MALICIOUS ATTACHMENT REMOVED - SBT.txt’. This is extremely unlikely to be the name of the real attachment - some Email Gateways have the ability to strip out and replace attachments to let recipients know it was malicious.
  
As the attachment is just a text file, we can open it without fear of malicious code execution.
</p>

<p> <img width="553" alt="image" src="https://github.com/RMBaez/Phishing-Response-Challenge/assets/170957530/498e2fb1-0520-4b48-be2a-908e7d23ce8c"> </p>

<p> 
- This informs us that the attachment was indeed malicious, and was actually an executable disguised as a PDF using the double extension ‘.pdf.exe’.

Here's our second malicious email, giving us the answer of ‘1, 3’.
</p>


<p> Email 4 </p>

<p> <img width="553" alt="image" src="https://github.com/RMBaez/Phishing-Response-Challenge/assets/170957530/f357ecb9-c83a-4b27-a56f-a3453203f9df"> </p>

<p> Based on the sender, styling, theme, and purpose of this email, we can classify this as spam/newsletter. The email is not using a real call-to-action despite a number of hyperlinks. Further analysis of the links could be conducted using tools such as URL2PNG or WHOis and reputation checks on the domain, however over time you'll learn to understand what is suspicious, and what is just spam.
</p>


<p> Email 5 </p>

<p> <img width="553" alt="Screenshot 2024-06-18 at 10 13 33 PM" src="https://github.com/RMBaez/Phishing-Response-Challenge/assets/170957530/1c0bc65d-e252-4a3e-a141-caa3b3300fea">
 </p>

<p> As with email four, we are seeing the same techniques being used. While parts of this email seem suspicious, such as the Reply-to address having the name set as ‘dfsdf’ and the subject line is misleading to individuals that aren't familiar with cryptocurrencies or investing, this is another spam email trying to convince people to sign up to begin trading cryptocurrencies, and is not inherently malicious - although it should be avoided!</p>



<p>
Question 2: First Malicious Email: What is the sending address?
</p>
<br />


<p>
<img width="434" alt="image" src="https://github.com/RMBaez/Phishing-Response-Challenge/assets/170957530/b7eb990a-f811-4e68-b32c-9cdaa83541e1">
  
  Opening Email One in Sublime Text and searching for (CTRL+F) ‘From’ we can find the sending email address, which is contained within the <> symbols at the end of the line (everything before this is just a friendly name that can be set as anything, only the final part matters!)
</p>



<p>
Question 3 - First Malicious Email: What is the subject line?
</p>
<br />


<p>
<img width="434" alt="image" src="https://github.com/RMBaez/Phishing-Response-Challenge/assets/170957530/3302c4f1-3a19-4374-99b7-b027b8cfde8d">
</p>

<p>A few lines below, or by searching for ‘Subject’ we can find the subject line.</p>


  
<p>
Question 4 - First Malicious Email: Who are the recipients? </p>
<br />


<p>
<img width="419" alt="Screenshot 2024-06-18 at 10 25 49 PM" src="https://github.com/RMBaez/Phishing-Response-Challenge/assets/170957530/5a384a37-1523-4e25-a83a-ea86b1a41563">

</p>

<p> Looking at line 42 we can see the email is being sent to jack.tractive@abcindustries.co.uk. </p>


<p>
Question 5. We'll search for the “X-Sender-IP” field and its value.
</p>
<br />

<p>
<img width="644" alt="image" src="https://github.com/RMBaez/Artifact-Extraction/assets/170957530/87334797-2169-41a0-ab51-21ad663cbe9c">
</p>

<p>
Question 6. Taking the IP from the previous question we'll open the site https://whois.domaintools.com and perform a search. We can see the resolved hostname below.
</p>
<br />


<p>
<img width="542" alt="Screenshot 2024-06-07 at 7 03 20 PM" src="https://github.com/RMBaez/Artifact-Extraction/assets/170957530/606c2bee-b9d7-4937-96b3-ac3985c8855e">
</p>

<p>
Question 7. The easiest way to retrieve this artifact is to right-click the hyperlink when viewing the file in an email client, and select ‘Copy Hyperlink’ (or a similar option).
</p>
<br />


<p>
<img width="546" alt="Screenshot 2024-06-07 at 7 07 02 PM" src="https://github.com/RMBaez/Artifact-Extraction/assets/170957530/1853f4e9-0aa3-4e26-8c31-b7108f382bd7">
</p>

<p>
Question 8. To find this we can either right-click the link in the email and select ‘copy link location’ and paste it into a program such as Notepad to see the URL text, or search for ‘http’ or ‘https’ in the email file until we find the right link. The ‘root domain’ essentially means the domain name of the URL, not including the specific resource. The root domain is ‘thiswouldbeamalicioussite.com’.
</p>
<br />


<p>
<img width="541" alt="image" src="https://github.com/RMBaez/Artifact-Extraction/assets/170957530/d3372b6e-a5fd-4ff9-a7ea-1d6f8eab9e7e">
</p>

<p>
Question 9. Same as before, we'll use Find and search for “From”.
</p>
<br />


<p>
<img width="541" alt="image" src="https://github.com/RMBaez/Artifact-Extraction/assets/170957530/4130de1d-f8d1-4989-8b95-55cd9459fd55">
</p>

<p>
Question 10. Searching for the “To” field and value.
</p>
<br />


<p>
<img width="541" alt="Screenshot 2024-06-07 at 7 16 25 PM" src="https://github.com/RMBaez/Artifact-Extraction/assets/170957530/81a51ff1-c4b0-4762-a267-57f33f238483">
</p>

<p>
Questoin 11. Searching for the “Subject” field and value.
</p>
<br />


<p>
<img width="541" alt="image" src="https://github.com/RMBaez/Artifact-Extraction/assets/170957530/eb374b24-2a0d-4522-83ec-b3ac31964d1b">
</p>
  
<p>
Question 12. Searching for the “Date” field and value.
</p>
<br />


<p>
<img width="334" alt="image" src="https://github.com/RMBaez/Artifact-Extraction/assets/170957530/a2c5d7fa-ed1c-4ae6-bd99-bb7fc8bd3b35">
</p>

<p>
Question 13. We'll search for the “X-Sender-IP” field and its value.
</p>
<br />


<p>
<img width="594" alt="image" src="https://github.com/RMBaez/Artifact-Extraction/assets/170957530/b02f5162-9866-431d-a731-0227cd9dc002">
</p>

<p>
Question 14. Using the IP from the previous question, we'll submit it to https://whois.domaintools.com.
</p>
<br />


<p>
<img width="545" alt="image" src="https://github.com/RMBaez/Artifact-Extraction/assets/170957530/480d7f9d-265c-4009-b913-894eacfefbe4">
</p>

<p>
Question 15. From within the text editor we can search for “filename”.
</p>
<br />

<p>
<img width="545" alt="image" src="https://github.com/RMBaez/Artifact-Extraction/assets/170957530/be2871cc-c8d6-41fa-9203-d2d422920b35">
</p>

<p>
Question 16. In Thunderbird we can right-click the attachment and click Save-As, then save it to the Desktop. We'll then open a PowerShell window and use the Get-FileHash cmdlet to retrieve the MD5 and SHA256 hashes. As SHA256 is the default hashing algorithm we don't need to state it, however we must do this for MD5.
</p>
<br />
