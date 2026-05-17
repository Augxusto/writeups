# Lab 06 - Access Control Vulnerability

## Information
> Difficulty: Easy <br>
> Date: 17-05-2026

---

## Objective
Log in using the credentials wiener:peter and exploit the flawed access controls to promote yourself to become an administrator.

### Explanation
Faça login usando uma conta de administrador e acesse o painel de administração para promover o usuário [Normal]
![panel-admin](images/login2026-05-17.png)

When we try to upgrade a user:
![admin-roles](images/admin-roles2026-05-17.png)

Now logout and log in with your Wiener username:
![wiener](images/wiener2026-05-17.png)

The intercepted administrative request was modified by changing the HTTP method from POST to GET and replacing the administrator session cookie with a standard user session cookie, successfully bypassing the access control validation:
![privilege escalation](images/escalation2026-05-17.png)
![solved](images/solved2026-05-17.png)