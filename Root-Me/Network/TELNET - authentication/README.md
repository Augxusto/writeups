# TELNET - authentication

## Information
> Difficulty: Easy <br>
> Date: 19-05-2026
---
### Objective
Find the user's password in this TELNET session capture.

---

### Explanation

<br>
Open the capture in Wireshark and apply the following filter to display only TELNET packets:

![telnet](<images/2026-05-19 232246.png>)

<br>
<br>

After filtering the traffic, follow the TELNET TCP stream to inspect the communication between the client and the server.

The credentials are transmitted in plaintext, allowing us to recover both the username and the password directly from the session:
![password](<images/2026-05-19 232256.png>)