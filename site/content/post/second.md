---
date: 2019-05-01T20:04:40.407Z
title: Petition Pronto
---
<h4>What is Petition Pronto?</h4>
Petition Pronto is a web application that allows students at Allegheny College to
submit a petition to professors (petitions are student submitted forms requesting
approval to add additional classes, remove classes, etc.). Professors are notified
by the website via an email that a petition request was submitted and decide
whether or not to approve the petitions or not. Depending on the decision, an email
will be sent to the student notifying them that their petition was either approved
or not. Currently, our program runs locally and so students will have to access
the tool from the terminal. To run the program, one would:

1. Navigate to the `\src` folder in terminal
2. Run `python3 app.py` (assuming python3 is installed)

<!--more...-->
---

<h4>My Contributions</h4>
Throughout the course of this project, I worked on creating a important piece of
functionality for the application: an email handler. Petition Pronto is exceptional
in that it sends emails to the students notifying them on whether or not their
petition was approved or not. The email handler went through several iterations
of refactored code until it was finally completely functional and was connected
to the database. Below is an excerpt of code from the module containing the email
handler of the project.

```
def send_email(subject, msg, EMAIL_RECIEVER):
    """Email a person with subject and message."""
    try:
        server = smtplib.SMTP('smtp.gmail.com:587')
        server.ehlo()
        server.starttls()
        server.login(config.EMAIL_ADDRESS, config.PASSWORD)
        message = 'Subject: {}\n\n{}'.format(subject, msg)
        server.sendmail(EMAIL_RECIEVER, EMAIL_RECIEVER, message)
        server.quit()
        print("Success: Email sent!")
    except:
        print("Email failed to send.")
```
The function `send_email` sends an email message containing a subject and a message.
The function takes three arguments: subject, message, and email receiver. We used
the smtp library to be able to access the email server and send emails to any student.
Those students are accessed from a text file that contains their names and their
student email address. When the email is sent, it will print `"Success: Email sent!"`.
However, in the event that the email does not go through, we will get `"Email failed
to send."`

<h4>Project Challenges</h4>
The biggest challenge that I faced with developing this software tool was configuring
the email handler. Initially we tested sending emails, but we were unable to send
it to only emails that were not associated with the college. We were able to
circumnavigate the problem in the end, but it turned out to not be a difficult fix.
Otherwise, the next biggest challenge was connecting the feature to the database,
but my teammates who were more familiar with flask were able to get that set up
easily.

Thank you for taking the time to learn about Petition Pronto and the work I've
put into it. If you're interested in learning more then please navigate to
the application's Github repository (see below).

Link to GitHub repository: https://github.com/GatorEducator/petition-pronto
