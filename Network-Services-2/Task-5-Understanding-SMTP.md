What is SMTP?

SMTP stands for "Simple Mail Transfer Protocol". It is utilised to handle the sending of emails. In order to support email services, a protocol pair is required, comprising of SMTP and POP/IMAP. Together they allow the user to send outgoing mail and retrieve incoming mail, respectively.

The SMTP server performs three basic functions:
	•  It verifies who is sending emails through the SMTP server.
	•  It sends the outgoing mail
	•  If the outgoing mail can't be delivered it sends the message back to the sender

Most people will have encountered SMTP when configuring a new email address on some third-party email clients, such as Thunderbird; as when you configure a new email client, you will need to configure the SMTP server configuration in order to send outgoing emails.

POP and IMAP

POP, or "Post Office Protocol" and IMAP, "Internet Message Access Protocol" are both email protocols who are responsible for the transfer of email between a client and a mail server. The main differences is in POP's more simplistic approach of downloading the inbox from the mail server, to the client. Where IMAP will synchronise the current inbox, with new mail on the server, downloading anything new. This means that changes to the inbox made on one computer, over IMAP, will persist if you then synchronise the inbox from another computer. The POP/IMAP server is responsible for fulfiling this process.

How does SMTP work?

Email delivery functions much the same as the physical mail delivery system. The user will supply the email (a letter) and a service (the postal delivery service), and through a series of steps- will deliver it to the recipients inbox (postbox). The role of the SMTP server in this service, is to act as the sorting office, the email (letter) is picked up and sent to this server, which then directs it to the recipient.

We can map the journey of an email from your computer to the recipient’s like this:

1. The mail user agent, which is either your email client or an external program. connects to the SMTP server of your domain, e.g. smtp.google.com. This initiates the SMTP handshake. This connection works over the SMTP port- which is usually 25. Once these connections have been made and validated, the SMTP session starts.

2. The process of sending mail can now begin. The client first submits the sender, and recipient's email address- the body of the email and any attachments, to the server.

3. The SMTP server then checks whether the domain name of the recipient and the sender is the same.

4. The SMTP server of the sender will make a connection to the recipient's SMTP server before relaying the email. If the recipient's server can't be accessed, or is not available- the Email gets put into an SMTP queue.

5. Then, the recipient's SMTP server will verify the incoming email. It does this by checking if the domain and user name have been recognised. The server will then forward the email to the POP or IMAP server, as shown in the diagram above.

6. The E-Mail will then show up in the recipient's inbox.
This is a very simplified version of the process, and there are a lot of sub-protocols, communications and details that haven't been included. If you're looking to learn more about this topic, this is a really friendly to read breakdown of the finer technical details- I actually used it to write this breakdown:
https://computer.howstuffworks.com/e-mail-messaging/email3.htm


What runs SMTP?

SMTP Server software is readily available on Windows server platforms, with many other variants of SMTP being available to run on Linux.

More Information:

Here is a resource that explain the technical implementation, and working of, SMTP in more detail than I have covered here.
https://www.afternerd.com/blog/smtp/

Answer the questions below

What does SMTP stand for?
How to: This can be found in the What is SMTP? section.
Answer: simple mail transfer protocol

What does SMTP handle the sending of? (answer in plural) 
How to: This can be found in the What is SMTP? section.
Answer: emails
 
What is the first step in the SMTP process?
How to: This can be found in the How does SMTP work? section. In the breakdown number 1.
Answer: SMTP handshake

What is the default SMTP port?
How to: This can be found in the How does SMTP work? section.  In the breakdown number 1.
Answer: 25

Where does the SMTP server send the email if the recipient's server is not available? 
How to: This can be found in the How does SMTP work? section.  In the breakdown number 4.
Answer: SMTP queue

On what server does the Email ultimately end up on?
How to: This can be found in the How does SMTP work? section.  In the breakdown number 5.
Answer: POP/IMAP

Can a Linux machine run an SMTP server? (Y/N) 
How to: This can be found in the What runs SMTP? section.
Answer: Y

Can a Windows machine run an SMTP server? (Y/N)
How to: This can be found in the What runs SMTP? section.
Answer: Y


From <https://tryhackme.com/room/networkservices2> 
