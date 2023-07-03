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



![image](https://github.com/ThuanNguyen115685/Report/assets/101619051/bc8d315c-b773-42f1-925f-75d38c8c36dd)



3. Save request with file name extension is `.txt`


![image](https://github.com/ThuanNguyen115685/Report/assets/101619051/eb77f770-7402-41e1-aa4d-b3b116f86a96)




 4. Use `sqlmap` with payload : 
  `python3 sqlmap.py -r poc.txt --risk 2 --dbms=MySQL --dbs --batch`


![image](https://github.com/ThuanNguyen115685/Report/assets/101619051/b4390493-7a68-4113-8e4f-3dd526ba1370)


![image](https://github.com/ThuanNguyen115685/Report/assets/101619051/5032b055-0e21-48ad-9d04-90b295c627c6)



# Impact:

A successful attack may result in the unauthorized viewing of user lists, the deletion of entire tables and, in certain cases, the attacker gaining administrative rights to a database.

