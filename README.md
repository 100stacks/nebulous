# Nebulous

#### Project ref: Cookiecutter Django (https://github.com/cookiecutter/cookiecutter-django)
#### Project ref: Cookiecutter CLI (https://github.com/cookiecutter/cookiecutter)

## Getting Started

- Setup project files
- Configure Postgres (other DBs are possible) database
- Launch local dev server
- Create a user
- Confirm user (via cli)
- Review Django Dashboard stats



## User Confirmation

- One of the setup options asks for your email service provider.  If you do not have one, you can use the local dev server as your friend.

![image](https://user-images.githubusercontent.com/10120600/139515827-18e4d369-beae-4b94-88bb-8fb03f6a7edf.png)

```
[29/Oct/2021 23:51:20] "GET /accounts/login/ HTTP/1.1" 200 15347
[29/Oct/2021 23:51:23] "GET / HTTP/1.1" 200 13840
[29/Oct/2021 23:51:37] "POST /accounts/login/ HTTP/1.1" 200 15503
[29/Oct/2021 23:51:43] "GET /accounts/signup/ HTTP/1.1" 200 15662
[29/Oct/2021 23:51:46] "GET / HTTP/1.1" 200 13840
[29/Oct/2021 23:52:10] "POST /accounts/signup/ HTTP/1.1" 200 15850
Content-Type: text/plain; charset="utf-8"
MIME-Version: 1.0
Content-Transfer-Encoding: 7bit
Subject: [Nebulous] Please Confirm Your E-mail Address
From: webmaster@localhost
To: test@example.com
Date: Fri, 29 Oct 2021 23:52:24 -0000
Message-ID: <163555154406.71794.8152055035143325499@Macbook.local>

Hello from Nebulous!

You're receiving this e-mail because user foo has given your e-mail address to register an account on example.com.

To confirm this is correct, go to http://0.0.0.0:8000/accounts/confirm-email/MQ:1mgbfc:nJaLJGyzdfu_bMewsKlo_NXXda6eEex2yqMJ5WwoM3g/

Thank you for using Nebulous!
example.com
-------------------------------------------------------------------------------
[29/Oct/2021 23:52:29] "POST /accounts/signup/ HTTP/1.1" 302 0
[29/Oct/2021 23:52:29] "GET /accounts/confirm-email/ HTTP/1.1" 200 14374
[29/Oct/2021 23:57:54] "GET /__debug__/render_panel/?store_id=3adadfd727a54a2380205486daef362b&panel_id=HistoryPanel HTTP/1.1" 200 41349
[29/Oct/2021 23:57:54] "GET /static/debug_toolbar/js/history.js HTTP/1.1" 200 1915
[29/Oct/2021 23:58:07] "GET /__debug__/render_panel/?store_id=3adadfd727a54a2380205486daef362b&panel_id=TemplatesPanel HTTP/1.1" 200 30231
[29/Oct/2021 23:58:12] "GET /__debug__/template_source/?template=account/base.html&template_origin=Ii9Vc2Vycy91c2VyMDAxL3Byb2plY3RzL3NhbmRib3gvbmVidWxvdXMvbmVidWxvdXMvdGVtcGxhdGVzL2FjY291bnQvYmFzZS5odG1sIg:1mgbfh:U4ZvUHkoTSZXcdXjJcpacbuY4ijYv4Wj5VAsl0kC_88 HTTP/1.1" 200 1894
[29/Oct/2021 23:58:25] "GET /accounts/confirm-email/ HTTP/1.1" 200 14125
[29/Oct/2021 23:58:25] "GET /static/images/favicons/favicon.ico HTTP/1.1" 200 8348
[29/Oct/2021 23:58:28] "GET / HTTP/1.1" 200 13840
```

Please notice the email template output from the local dev server:

```
To confirm this is correct, go to http://0.0.0.0:8000/accounts/confirm-email/MQ:1mgbfc:nJaLJGyzdfu_bMewsKlo_NXXda6eEex2yqMJ5WwoM3g/
```

![image](https://user-images.githubusercontent.com/10120600/139515873-cb948bc2-291f-411c-93b2-e904a6e26501.png)

## `DJango` Dashboard

### History - `foo` user
![image](https://user-images.githubusercontent.com/10120600/139516034-c3a4b112-d0ca-40e3-b5d5-da5bc16b5a95.png)

### Let's see the server output...

![image](https://user-images.githubusercontent.com/10120600/139516077-d1c4d62f-53bc-4255-b8db-b20e7f5fb019.png)

### Request Headers

![image](https://user-images.githubusercontent.com/10120600/139550094-cc269307-8941-4d06-92cc-bb755b6556c5.png)

### PostgreSQL Queries

![image](https://user-images.githubusercontent.com/10120600/139551549-cc426de5-e32e-4c5a-bc02-7df28154e476.png)

