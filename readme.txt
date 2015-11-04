INSTUCTION FOR JENKINS, GRID HEARTBEAT

PREQUESTED
	- Java 1.8 (added to your Windows PATH)
	- Administrator priviliges
	

INSTALATION
 - download and unzip package
 - there are two bat files:
	- start-service.bat
	- stop-service.bat

	
 - to start Heartbeat open command prompt as an administrator
	- navigate to /paht/to/downloaded/package/heartbeat
	- write start-service.bat 
	
 - to stop Heartbeat open command prompt as an administrator
	- navigate to /paht/to/downloaded/package/heartbeat
	- write stop-service.bat 

CONFIGURATION
 - report.csv is the Heartbeat report
 - in /heartbeat/heartbeat there are three configuration files:
 
 - heartbeat.properties - application properties
 - grid.json - configuration of grid servers
 - jenkins.json - configuration of jenkins servers
 
 - to change frequency of application running set proper values in:
	delay.hour
	delay.minute
	delay.seconds
 - to change directory of your report.csv use:
	csv.report
 - to change directory of your jenkins.json use:
	jenkins.json
 - to change directory of your grid.json use:
	grid.json
	
 - to configure jenkins test, follow the convention in jenkis.json:
	- url - stands for the addres of Jenkins server
	- username - is username that has rights to run a job
	- password - is password for username
	- jobname - name for job you want to test (for best create some mock job and pass the name here)
	
- to configure grid test, follow the convention in grid.json:
	- url - stands for the addres of Grid Hub 
	- nodes - are registered nodes that you want to test
		- browser - name of browser
		- browserVersion - version
		- platform - system 
		
		REMBER TO USE ALREADY REGISTERED NODES

 - if you want to reconfigure either jenkins.json, grid.json or heartbeat.properties:
	- stop service 
	- change configuration that you want
	- start service
	
- PLEASE DO NOT MODIFY report.csv - if you want to reuse it simply make a copy.
