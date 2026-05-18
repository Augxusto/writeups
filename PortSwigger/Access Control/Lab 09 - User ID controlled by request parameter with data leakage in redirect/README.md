# Lab 09 - Access Control Vulnerability

## Information
> Difficulty: Easy <br>
> Date: 18-05-2026
---
### Objective
 This lab contains an access control vulnerability where sensitive information is leaked in the body of a redirect response.
To solve the lab, obtain the API key for the user carlos and submit it as the solution. 

### Explanation
**Login as user wiener:**

![login](images/login-09-2026-05-17.png)
**After authentication, I navigated to the My Account page.**


**Intercepting the request**
Using Burp Suite, I intercepted the request sent when accessing the account page.
The application used the user identifier directly in the request:

![my account](images/my-account-wiener2026-05-18.png)


**Modifying the parameter for carlos:**

![change](images/parameter-carlos2026-05-18.png)
![302-found](images/302-found2026-05-18.png)
![api](images/api-carlos2026-05-18.png)
![solved](images/solved-lab09-2026-05-18.png)



### Conclusion

The application was vulnerable to Broken Access Control because it exposed sensitive information in the body of a redirect response without properly validating user authorization.