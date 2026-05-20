# Lab 10 - Access Control Vulnerability

## Information
> Difficulty: Easy <br>
> Date: 20-05-2026
---
### Objective
This lab contains a user account page that displays the current user's existing password in a prefilled masked input field.

To solve the lab, retrieve the administrator's password and use it to delete the user `carlos`.

### Explanation
<br>

**When logging in with a standard user, we can change the `id` parameter in the URL to `administrator`:**
<br>

![id-parameter](<images/Captura de tela 2026-05-20 153238.png>)
<br>

![adm-page](<images/Captura de tela 2026-05-20 152731.png>)

<br>
<br>



### The modified request can be sent to Repeater in Burp Suite for further analysis.

**After inspecting the server response, the administrator account information is disclosed in the HTML response body, including the administrator password.**
![burp](<images/Captura de tela 2026-05-20 153103.png>)
![f12](<images/f122026-05-20 154251.png>)

<br>
<br>

### When we login using an administrator account, we get 1 additional feature, namely : Admin Panel.

![solved](<images/solved2026-05-20 154437.png>)V