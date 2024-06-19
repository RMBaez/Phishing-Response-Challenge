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


<p>
<img <img width="538" alt="image" src="https://github.com/RMBaez/Artifact-Extraction/assets/170957530/fdc12ecd-417a-43ce-9efb-4dff452d34f6">
</p>

<p>
Question 2. We'll look for the “To” field and its value.
</p>
<br />


<p>
<img width="538" alt="image" src="https://github.com/RMBaez/Artifact-Extraction/assets/170957530/c9b0fac7-16b3-4218-a7b5-c6f2b32dd2ce">
</p>

<p>
Questoin 3. We'll look for the “Subject” field and its value.
</p>
<br />


<p>
<img width="538" alt="Screenshot 2024-06-07 at 6 58 41 PM" src="https://github.com/RMBaez/Artifact-Extraction/assets/170957530/6df98f18-4519-426e-8f05-9087ef66ed1c">
</p>
  
<p>
Question 4. We'll look for the “Date” field and its value.
</p>
<br />


<p>
<img width="538" alt="Screenshot 2024-06-07 at 6 58 41 PM" src="https://github.com/RMBaez/Artifact-Extraction/assets/170957530/9a987c11-1887-4498-bba8-ae599c365659">
</p>

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
