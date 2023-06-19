# Summary: 

SQL injection is an attack technique that exploits a security vulnerability occurring in the database layer of an application

# Description:

SQL injection is a vulnerability that allows an attacker to alter backend SQL statements by manipulating the user input.

# POC

Steps To Reproduce:

  1.   Go to : http://localhost/php-inventory-management-system/index.php .

![image](https://github.com/ThuanNguyen115685/Report/assets/101619051/2a7349fd-6322-4c91-9238-f4645715fea1)

  2.  Input `Username : admin` and `Password: 123`, then use `Burp Suite` and press button `Sign in` to Intercept request.

 ![image](https://github.com/ThuanNguyen115685/Report/assets/101619051/681a4459-773f-4699-99b1-cb8355572cc5)

![image](https://github.com/ThuanNguyen115685/Report/assets/101619051/a616ef24-ad32-4e86-997b-a191124a6406)

  3. Save request with file name extension is `.txt`

![image](https://github.com/ThuanNguyen115685/Report/assets/101619051/dbaed971-bb81-45a1-bf17-27bcdce5bee2)

  4. Use `sqlmap` with payload : 
  `python3 sqlmap.py -r poc.txt --random-agent  --tamper=space2comment --risk 2 --level 2 --dbms=MySQL -dbs`
  
![image](https://github.com/ThuanNguyen115685/Report/assets/101619051/7a8fca73-f315-46ae-8210-e4e9dd73035f)

![image](https://github.com/ThuanNguyen115685/Report/assets/101619051/ba85a3cd-e1bd-4231-82b5-e022bb1cc046)

# Impact:

A successful attack may result in the unauthorized viewing of user lists, the deletion of entire tables and, in certain cases, the attacker gaining administrative rights to a database.
