# Bypassing 403 Protection To Get Pagespeed Admin Access

## General Methods :

[Bypassing 403 Protection To Get Pagespeed Admin Access](https://sapt.medium.com/bypassing-403-protection-to-get-pagespeed-admin-access-822fab64c0b3)

Adding Headers and paths which you can use to bypass 403 restrictions

1. **Adding in URL paths** : Adding path of the URL and the file which is forbidden
- /*
- /%2f/
- / ./
- /* /

1. **Adding Headers in request** : Adding different headers in request with value 127.0.0.1 can also help in bypassing restriction  

- X-Custom-IP-Authorization
- X-Forwarded-For
- X-Forward-For
- X-Remote-IP
- X-Originating-IP
- X-Remote-Addr
- X-Client-IP
- X-Real-IP

1. **Changing request Method** : Changing request from GET to POST also leads to bypass

---

## **His Case :**

[https://target](https://pagespeed.com)/pagespeed_admin  →  it was 403 forbidden

Using specified methods via [**automated tool](https://github.com/iamj0ker/bypass-403) → Found that in one case response code changed from 403 → 200 testing it manually in browser and  it finally Bypass.**

 **Method : [https://target//pagespeed_admin](https://target//pagespeed_admin) → Just adding a single slash after target bypass the 403 and got complete access to pagespeed admin.**

 

This was taken as P2-High Severity.