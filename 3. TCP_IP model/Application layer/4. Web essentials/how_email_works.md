# How Email Works


Email works using a combination of protocols that allow messages to be sent, received, and stored. When you send an email, it goes through several steps before reaching the recipient.
 SMTP is built on top of TCP, but it adds additional features and functionality tailored to email delivery.

## Steps of Sending an Email
1. **Composing and Sending:**
   - A user writes an email and clicks "Send" in an email client (e.g., Gmail, Outlook).
   - The email client connects to an **SMTP (Simple Mail Transfer Protocol) server**.

2. **SMTP Server Processing:**
   - The SMTP server checks the recipient's email address domain (e.g., `@gmail.com`, `@yahoo.com`).
   - If the recipient is on the same domain, it delivers the email directly.
   - If the recipient is on a different domain, it looks up the recipient's **Mail Exchange (MX) records** using DNS.

3. **Email Routing:**
   - The SMTP server forwards the email to the recipient's email provider's SMTP server (e.g., Gmail's or Yahoo's mail server).
   - The email is then stored on the recipient's email server.

4. **Receiving the Email:**
   - The recipient's email client retrieves the email using **IMAP (Internet Message Access Protocol) or POP (Post Office Protocol)**.
   - The user can now see the email in their inbox.

---

# POP Protocol (Post Office Protocol)

## What is POP?
**POP (Post Office Protocol)** is a protocol used by email clients to retrieve emails from a mail server.

### How POP Works:
1. The email client connects to the mail server and downloads new emails.
2. Emails are **removed from the server** and stored locally on the user's device (unless configured to keep a copy on the server).
3. The user can access emails only on the device where they were downloaded.

### POP vs. IMAP:
| Feature       | POP | IMAP |
|--------------|-----|------|
| Email stored on | Local device | Mail server |
| Access from multiple devices | No | Yes |
| Offline Access | Yes | Limited |
| Syncs across devices | No | Yes |

**POP is best for users who want to download emails and free up server storage, while IMAP is better for accessing emails from multiple devices.**

---

# What Happens When I Send an Email?

## Case 1: Sending an Email to `@gmail.com`
1. Your email client sends the email to Gmail's SMTP server.
2. The SMTP server checks that the recipient is also on Gmail.
3. The email is delivered to the recipient's inbox on Gmail's mail servers.
4. The recipient retrieves the email using Gmail's webmail, IMAP, or POP.

## Case 2: Sending an Email to `@yahoo.com`
1. Your email client sends the email to Gmail's SMTP server.
2. Gmail’s SMTP server checks the **DNS MX record** for `yahoo.com`.
3. It finds Yahoo’s mail server (e.g., `mx.mail.yahoo.com`).
4. The email is transferred to Yahoo’s SMTP server.
5. Yahoo delivers the email to the recipient’s inbox.
6. The recipient retrieves the email using Yahoo’s webmail, IMAP, or POP.

---

## Why Do We Need SMTP Instead of Just TCP?

1. **Specialized for Email Communication**:
   - SMTP defines how email messages are formatted, addressed, and routed to ensure correct delivery.
   - Unlike TCP, which simply transfers raw data, SMTP structures the data into email formats with headers (like `From`, `To`, `Subject`) and body content.

2. **Routing Emails to the Right Server**:
   - SMTP handles the process of **email routing** based on domain names (e.g., `@gmail.com` or `@yahoo.com`).
   - It looks up the destination mail server (MX records in DNS) and delivers the email to the appropriate server, something TCP alone cannot do.

3. **Handling Queues and Retry Mechanisms**:
   - If an email cannot be delivered (e.g., due to server downtime), SMTP has mechanisms to queue the message and retry delivery later.
   - TCP cannot handle this scenario directly; it simply ensures packets are sent and received, but does not track the state of message queues or retries for specific application purposes like email.

4. **Session Management**:
   - SMTP establishes a session between the sender and receiver's mail servers, ensuring that the email transfer process is carried out correctly.
   - TCP, on the other hand, is a lower-level protocol that simply handles the transport of data without understanding the application logic like email handling.

5. **Mail-Related Commands**:
   - SMTP includes commands like `HELO`, `MAIL FROM`, `RCPT TO`, and `DATA` that define how an email should be sent.
   - These commands structure the communication between the email client and server, guiding the email transfer process. TCP, in contrast, does not have these predefined commands.

## Summary
- **SMTP** is specifically designed for email communication, providing the necessary structure, routing, session management, and error handling to ensure reliable email delivery.
- Emails are sent using **SMTP** and retrieved using **IMAP or POP**.
- **POP** downloads emails and removes them from the server, making them accessible only on one device.
- Sending an email to a different domain (`@gmail.com` → `@yahoo.com`) involves DNS lookup and routing through SMTP servers.
