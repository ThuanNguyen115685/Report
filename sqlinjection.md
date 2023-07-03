# Summary:
SQL injection is an attack technique that exploits a security vulnerability occurring in the database layer of an application

# Description:
SQL injection is a vulnerability that allows an attacker to alter backend SQL statements by manipulating the user input.

# POC

Steps To Reproduce:


1. Go to : http://localhost/NEWS-BUZZ-master/


![image](https://github.com/ThuanNguyen115685/Report/assets/101619051/db8135f1-ec33-4525-9d33-13fbac76e537)


2.  Input `Username : username` and `Password: 123`, then use `Burp Suite` and press button `Submit` to Intercept request.


![image](https://github.com/ThuanNguyen115685/Report/assets/101619051/3797f472-5619-4a1f-b0e7-cd234ec52297)



![image](https://github.com/ThuanNguyen115685/Report/assets/101619051/2bb093aa-ecb7-43b3-b017-17a8cd1a9a9c)


3. Save request with file name extension is `.txt`


![image](https://github.com/ThuanNguyen115685/Report/assets/101619051/ad32ccb0-21aa-47ae-9e5b-3347664c4ecc)


 4. Use `sqlmap` with payload : 
  `python3 sqlmap.py -r newsbuzz.txt --risk 2 --dbms=MySQL --dbs --batch`


![image](https://github.com/ThuanNguyen115685/Report/assets/101619051/60ea8dfc-638f-4edb-91c5-6139ede6ae9c)


![image](https://github.com/ThuanNguyen115685/Report/assets/101619051/1a899945-0f59-45cb-825d-49f5fb7b74bf)


# Impact:

A successful attack may result in the unauthorized viewing of user lists, the deletion of entire tables and, in certain cases, the attacker gaining administrative rights to a database.

