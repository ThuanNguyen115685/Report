Summary:

Reflected cross-site scripting (or XSS) arises when an application receives data in an HTTP request and includes that data within the immediate response in an unsafe way.

Description:

Reflected XSS attacks, also known as non-persistent attacks, occur when a malicious script is reflected off of a web application to the victim's browser.

Steps To Reproduce:

1.  Go to http://localhost/php-inventory-management-system/index.php
![image](https://github.com/ThuanNguyen115685/Report/assets/101619051/a7e34caf-3c9d-455a-9d29-2b05cd21d47e)

2.  On the url, enter payload after url: `cuzh4"><script>alert('VIETNAM')</script>rvhmf`

    Payload: http://localhost/php-inventory-management-system/index.php/cuzh4"><script>alert('VIETNAM')</script>rvhmf
![image](https://github.com/ThuanNguyen115685/Report/assets/101619051/cf81a84c-5b2f-482a-baf2-2fac74c25c3b)

Impact:

The impact of reflected cross-site scripting (XSS) can be significant and pose various risks to both web applications and users
