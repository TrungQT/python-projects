import smtplib
import ssl
from email.message import EmailMessage

# Sender
email_sender = ''
# App password - Use app password after setting up 2-step verification
email_password = ''
#Send to
email_receiver = ''

# Set the subject and body of the email
subject = 'Hello!'
body = """
I am sending this email using Python!
"""

email_message = EmailMessage()
email_message['From'] = email_sender
email_message['To'] = email_receiver
email_message['Subject'] = subject
email_message.set_content(body)

# Add SSL (layer of security)
context = ssl.create_default_context()

# Log in and send the email
with smtplib.SMTP_SSL('smtp.gmail.com', 465, context=context) as smtp:
    smtp.login(email_sender, email_password)
    smtp.sendmail(email_sender, email_receiver, email_message.as_string())
