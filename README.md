```
NAME : MURALI KRISHNA S
REGISTER NUMBER : 212223230129
DEPT : ARTIFICIAL INTELLIGENCE AND DATA SCIENCE
```
# Metasploit-for-reconnaissance
# Metasploit
Metasploit for reconnaissance in pentesting

# AIM:

To get introduced to Metasploit Framework and to  perform reconnaissance  in pentesting .

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

## EXECUTION STEPS AND ITS OUTPUT:

### Find out the ip address of the attackers system


## OUTPUT:

![ID](https://github.com/user-attachments/assets/848ab409-1757-4c52-bc46-8a527b522c1d)



### POSTGRESQL

## OUTPUT:

![02](https://github.com/user-attachments/assets/6733bfd4-ca47-4ca8-9cfc-c297da8bcaef)

### msfdb :

### OUTPUT:

![03](https://github.com/user-attachments/assets/c4b60fc9-1171-434c-9b33-a3b89c5c5a23)

### Invoke msfconsole:

### OUTPUT:

![001](https://github.com/user-attachments/assets/647debb8-8a74-4633-bb09-ce1b598f75e1)

Type help or a question mark "?" to see the list of all available commands you can use inside msfconsole.

### OUTPUT:

![05](https://github.com/user-attachments/assets/d3ca4023-a5cf-49d3-a011-2749a259236e)

### PORT SCANNING:

Following command is executed for scanning the systems on our local area network with a TCP scan (-sT) looking for open ports between 1 and 1000 (-p1-1000). msf > nmap -sT 192.168.1810/24 -p1-1000

### OUTPUT:

![06](https://github.com/user-attachments/assets/63964cb0-b72b-49bf-bb0d-660275a0f93a)

### Step 4:

use the db-nmap command to scan and save the results into Metasploit's postgresql attached database. In that way, you can use those results in the exploitation stage later.

scan the targets with the command db_nmap as follows. msf > db_nmap 192.168.181.0/24

### OUTPUT:

![08](https://github.com/user-attachments/assets/8b17747b-e62a-4009-87fe-cd54dec03c16)


Metasploit has a multitude of scanning modules built in. If we open another terminal, we can navigate to Metasploit's auxiliary modules and list all the scanner modules. cd /usr/share /metasploit-framework/modules/auxiliary kali > ls -l

### OUTPUT:

![09](https://github.com/user-attachments/assets/787b0596-76c5-4c6a-8ed4-001bb0147a97)

Search is a powerful command in Metasploit that you can use to find what you want to locate. msf >search name:Microsoft type:exploit

### OUTPUT:

![10](https://github.com/user-attachments/assets/855d4e0e-8f66-4877-815d-eb5b2b00feeb)

The info command provides information regarding a module or platform,

### OUTPUT:

![11](https://github.com/user-attachments/assets/042d255c-029d-4e6a-a714-a64a5b77f0cb)

The info command provides information regarding a module or platform,

### MYSQL ENUMERATION

Find the IP address of the Metasploitable machine first. Then, use the db_nmap command in msfconsole with Nmap flags to scan the MySQL database at 3306 port. db_nmap -sV -sC -p 3306 <metasploitable_ip_address>

### OUTPUT:

![12](https://github.com/user-attachments/assets/99bb804f-3a7e-4355-a48d-a48045c57ac1)

Use the search option to look for an auxiliary module to scan and enumerate the MySQL database. search type:auxiliary mysql

### OUTPUT:

![13](https://github.com/user-attachments/assets/97a63214-9b39-4adb-b06c-ed71532d9209)

use the auxiliary/scanner/mysql/mysql_version module by typing the module name or associated number to scan MySQL version details. use 11 Or: use auxiliary/scanner/mysql/mysql_version

### OUTPUT:

![14](https://github.com/user-attachments/assets/15d5b05a-d093-4386-8761-b930f6ef3451)

Use the set rhosts command to set the parameter and run the module, as follows:

### OUTPUT:

![15](https://github.com/user-attachments/assets/2c1f065d-0a93-4280-807a-9704d2fb360d)

After scanning, you can also brute force MySQL root account via Metasploit's auxiliary(scanner/mysql/mysql_login) module.

### OUTPUT:

![16](https://github.com/user-attachments/assets/6d7060e7-25a7-49f0-b066-3306691f08d1)

set the PASS_FILE parameter to the wordlist path available inside /usr/share/wordlists: set PASS_FILE /usr/share/wordlistss/rockyou.txt Then, specify the IP address of the target machine with the RHOSTS command. set RHOSTS Set BLANK_PASSWORDS to true in case there is no password set for the root account. set BLANK_PASSWORDS true

### OUTPUT:

![18 l](https://github.com/user-attachments/assets/c3782d96-f467-4873-8cf7-684311028236)

## RESULT:
The Metasploit framework for reconnaissance is  examined successfully

