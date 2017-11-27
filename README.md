# Expcamera
Exploit Netwave and GoAhead IP Camera  
Expcamera is a tool for exploiting vulnerable Netwave and GoAhead IP camera to get the username and password.  
**Attention:this tool is just for educational!  **
**Please comply with local laws and regulations!  **

# Installation
	git clone https://github.com/vanpersiexp/expcamera.git  
	pip3 install -r related.txt  
# Usage
	python3 exploit_camera.py -h  

	usage: exploit_camera.py [-h] [-b {1,2}] [-o OUTPUTFILE] [-T TIMEOUT]  
        	                 [-t TASKS] [-q | -v] [-i IP | -I INPUTFILE]  

	Exploit IP Camera. Please use it just in educational purpose!  

	optional arguments:  
	  -h, --help     show this help message and exit  
	  -b {1,2}       Choose the brand of IP Camera. 1 represents Netwave,2  
	                 represents GoAhead.  
	  -o OUTPUTFILE  Output into path you input.The default path in dir /tmp  
	  -T TIMEOUT     The default timout for netwave is 300s.  
	  -t TASKS       Run TASKS number of connects in parallel,default is 10  
	  -q             Quiet mode.  
	  -v             Show more informations.  
	  -i IP          The camera's ip and port.Example: 192.168.1.100:80  
	  -I INPUTFILE   The camera's ip:port address file. The file's format like  
	                 this 192.168.1.100:80 in a line.  
# Example
	1.Victim IP Camera's brand is Netwave.The ip is 192.168.1.100 and port is 80
	python3 exploit_camera.py -b 1 -i 192.168.1.100:80 -v
	2.Victim IP Camera's brand is GoAhead.The iplist.txt is given.
	The iplist.txt show as below:
	192.168.1.10:80
	192.168.1.100:81
	192.168.1.200:8080
	python3 exploit_camera.py -b 2 -I iplist.txt -v
	
# Contacts
pu.xiaorvp@gmail.com  

# References
http://www.cnvd.org.cn/flaw/show/CNVD-2017-01037  
http://cn.0day.today/exploit/26889  
https://pierrekim.github.io/blog/2017-03-08-camera-goahead-0day.html  
