# UiARD_FirstProcess

1.	This workflow retrieves all unread emails, from the Outlook account in use, that have 'Course Invoices in the subject line.
2.	At the beginning of this process, an ‘Input Dialog’ message will appear requesting your email address.
3.	It will then go to the "https://acme-test.uipath.com/first-automation" webpage, ‘Part 1’ and click ‘Notify Me’.
4.	It will automatically input your email address.
5.	You will have to solve the Captcha and then click ‘Submit’.
6.	The automation will keep running the ‘Get Outlook Mail Messages’ activity until there are 4 invoices in your email account.
7.	Emails retrieved are saved under the 'CourseEmails' list in MailMessage type of variable.
8.	Afterwards, attachments for each mail message retrieved are saved in a new project folder, titled 'Invoices'.
9.	It then identifies and copies the client code from each attachment and stores it under the 'ClientCode' variable.
10.	Next, using the Chrome browser, it accesses the "https://acme-test.uipath.com/first-automation" webpage, clicks 'Part 2' and types in the client code to get the discount value.
11.	The discount value is stored under the 'DiscountValue' variable (this operation is repeated for all stored client codes).
12.	If the discount value contains the "$" character, the value will be typed in the 'Invoice' sheet, in the 'E18' cell. Otherwise, the value "$0" will be added.
13.	Next the 'RPA, Dev, Alex.Sushko@uipath.com" signature is added in each of the invoice sheets.
14.	Finally, write the text to be used to prepare an Outlook draft email containing the updated invoices (the draft email can be found inside the 'Drafts' folder of the Outlook account in use).


Activities Used:
- Input Dialog
- User Application/Browser
- Click
- Type Into
- Delay
- Do While
- Log Message
- Get Outlook Mail Message
- For Each
- Read Cell
- Get Text
- If / Then
- Write Cell
- Use Desktop Outlook App
- Message Box
