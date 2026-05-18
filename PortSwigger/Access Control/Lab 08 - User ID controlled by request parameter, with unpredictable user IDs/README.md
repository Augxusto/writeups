# Lab 08 - Access Control Vulnerability


## Information

> Difficulty: Easy <br>
> Date: 18-05-2026



# Objective
This lab has a horizontal privilege escalation vulnerability on the user account page, but identifies users with GUIDs.

To solve the lab, find the GUID for carlos, then submit his API key as the solution.

## Exploitation
**Home page:**

![home-page](images/home-page2026-05-18.png)

**Login as user wiener:**

![login](images/login-07-2026-05-17.png)

**In the home page, we can view Carlos's post:**

![post](images/post2026-05-18.png)
![carlos-post](images/carlos-post2026-05-18.png)

**While viewing Carlos's blog post, the application exposed his user identifier (GUID) in the request URL:**
```html
<p><span id=blog-author><a href='/blogs?userId=904f9ed7-69b1-aedf-4ffddec86e0c'>carlos</a></span> | 23 April 2026</p>
```


**Using Burp Suite, it was possible to intercept the request and obtain Carlos's GUID.**
**After identifying the GUID, the /my-account endpoint was modified to reference Carlos's identifier instead of the current authenticated user:**

![carlos-id](images/carlos-id2026-05-18.png)

**The server returned Carlos's account page, including his API key:**

![api-key](images/change-id2026-05-18.png)

![solved](images/solved-lab82026-05-18.png)