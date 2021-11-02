# Account take over

For account take over we need two email ID's first is attacker@gmail.com and victim@gamil.com

## What is this ?

- Enter email you want to reset the password
- Click on reset password
- We will have Confirmation code in our email.
- Let's go to Confirmation page and confirm it.
- And you are able to change your password.

## Flaw in this logic which lead to account take over ?

Let's assume we want to reset attacker@gmail.com password.

1. We entered the email.
2. we have Confirmation code & Confirmation page.
3. Let's enter  correct code in confirmation page and **intercept the request in Burp Suite. [ Right Click > Do intercept > Response to this request.]**
4. **Now copy the response and save it for future use** [ This is the response when code is correct ]
5. Now Let's start again but this time email is **victim@gmail.com**
6. This time when we are going to reset password of **victim@gmail.com.** 
7. We are going to enter incorrect confirmation code and intercept this request and response to this request.
8. This is the response when confirmation code is incorrect.
9. Now replace incorrect response with the previous correct response and click forward.
10. Now simple write a new password save it then try to login with victim@gmail.com with new password. 

If you will successfully login account with new password the **Account takeover successful.**