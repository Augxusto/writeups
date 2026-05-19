# FTP - authentication

## Information
> Difficulty: Easy <br>
> Date: 19-05-2026
---
### Objective
An authenticated file exchange achieved through FTP. Recover the password used by the user.

---

### Explanation

<br>
Download the challenge file:

![download](images/download2026-05-19.png)

<br>
<br>
Open the capture in Wireshark and apply the following filter to display only FTP packets:

![filter-ftp](images/filter-ftp2026-05-19.png)

<br>
<br>
While analyzing the FTP traffic, we can identify the PASS command, which contains the user's password in plaintext.

Select the packet and inspect its contents:

![traffic of ftp pass](<images/traffic of ftp pass2026-05-19.png>)

<br>
<br>
Done:

![copy and past password](<images/copy and past password2026-05-19.png>)