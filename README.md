# Expcamera
Exploit Netwave and GoAhead IP Camera  
Expcamera is a tool for exploiting vulnerable Netwave and GoAhead IP camera to get the username and password.  
Environment:Linux,Python3  
	
**Attention:this tool is just for educational!**  
**Please comply with local laws and regulations!**  

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
1.Victim IP Camera's brand is Netwave.The ip is 192.168.1.100 and port is 80.  

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
http://www.cert.org.cn/publish/main/9/2017/20170320152751379105282/20170320152751379105282_.html  


# 中文版
Netwave和GoAhead多款摄像头密码泄漏漏洞的利用工具。  
本工具用于针对仍未修补漏洞的摄像头，可以获取摄像头的管理员账户和密码。  
使用环境：Linux,Python3。  

**注意：此工具只用于学习交流目的。**  
**请严格遵守您所在国家的法律法规！**  

# 安装
	git clone https://github.com/vanpersiexp/expcamera.git  
	pip3 install -r related.txt  
# 使用
	python3 exploit_camera.py -h  

	usage: exploit_camera.py [-h] [-b {1,2}] [-o OUTPUTFILE] [-T TIMEOUT]  
        	                 [-t TASKS] [-q | -v] [-i IP | -I INPUTFILE]  

	Exploit IP Camera. Please use it just in educational purpose!  

	optional arguments:  
	  -h, --help     show this help message and exit.帮助信息   
	  -b {1,2}       Choose the brand of IP Camera. 1 represents Netwave,2  
	                 represents GoAhead.选择摄像头品牌，1代表Netwave，2代表GoAhead。  
	  -o OUTPUTFILE  Output into path you input.The default path in dir /tmp.输出文件路径，默认为/tmp  
	  -T TIMEOUT     The default timout for netwave is 300s.默认超时时间为300s。  
	  -t TASKS       Run TASKS number of connects in parallel,default is 10.多任务同时处理，默认为10。  
	  -q             Quiet mode.安静模式。  
	  -v             Show more informations.显示更多信息。    
	  -i IP          The camera's ip and port.Example: 192.168.1.100:80.摄像头ip和port形式。例如：192.168.1.100:80。    
	  -I INPUTFILE   The camera's ip:port address file. The file's format like  
	                 this 192.168.1.100:80 in a line.摄像头ip和port文件格式。每一行都以192.168.1.100:80的形式。 
 
# 例子
1.摄像头品牌为Netwave。IP地址为192.168.1.100, port端口为80。  

	python3 exploit_camera.py -b 1 -i 192.168.1.100:80 -v  

2.摄像头品牌为GoAhead。IP地址文件iplist.txt如下所示：  
192.168.1.10:80  
192.168.1.100:81  
192.168.1.200:8080  

	python3 exploit_camera.py -b 2 -I iplist.txt -v
	
# 联系方式
pu.xiaorvp@gmail.com  

# 参考
http://www.cnvd.org.cn/flaw/show/CNVD-2017-01037  
http://cn.0day.today/exploit/26889  
https://pierrekim.github.io/blog/2017-03-08-camera-goahead-0day.html  
http://www.cert.org.cn/publish/main/9/2017/20170320152751379105282/20170320152751379105282_.html  


