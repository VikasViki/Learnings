## Week 1 : Cookies and Sessions

- cookies are stored in form of dictinoary inside ***request.COOKIES***.
- ***set_cookies()*** method sets the cookie inside the browser, ***max_age*** parameter is used specify the expiration time for the cookie in number of seconds, be default the cookie remains till the browser is closed.
- sessions are stored inside session table as base64 encoded keys.
- similar to cookies session can also be accessed through ***request.session***.