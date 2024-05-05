-> Install jenkins 
    - clone code from git
-> Install docker pipeline plugin - Docker Pipeline
-> Install SonarQube 
	- Install Sonar plugin - SonarQube Scanner
	- Configure a Sonar Server locally
	- Add user - password is => sonar@123
	- Go to the user => sudo su - sonarcube
	- download => wget https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.4.0.54424.zip
	- Unzip => unzip *
		chmod -R 755 /home/sonarqube/sonarqube-9.4.0.54424
		chown -R sonarqube:sonarqube /home/sonarqube/sonarqube-9.4.0.54424
		cd sonarqube-9.4.0.54424/bin/linux-x86-64/
		./sonar.sh start 
	- Access the SonarQube with <IP:9000> - Pwd would be admin/admin - change password => sonar@123
	-> To authenticate sonar with Jenkins
		- Go to, sonarqube click on My Account -> Security -> provide the Token Name and Generate it and copy the token
		- Go to, Jenkins -> Manage jenkins -> Credentials -> system -> Global Credentials -> Add credentials
-> Install Docker
	- apt install docker.io
	- Grand the permissions
		usermod -aG docker jenkins
		usermod -aG docker ubuntu
		systemctl restart docker
	- Restart Jenkins - http://35.239.225.236:8080/restart	
