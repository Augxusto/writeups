# Lab 07 - Access Control Vulnerability


## Information

> Difficulty: Easy <br>
> Date: 17-05-2026


# Objective

This lab has a horizontal privilege escalation vulnerability on the user account page, but identifies users with GUIDs.

## Exploitation

Login using the credentials wiener:peter

### Explanation

Login as user wiener:

![login](images/login-07-2026-05-17.png)


Changing the id wiener to carlos directly in the URL:

![change-id](images/parameter-2026-05-17.png)

Carlos API:

![api](images/api2026-05-17.png)

![solved](images/solved-2026-05-17.png)