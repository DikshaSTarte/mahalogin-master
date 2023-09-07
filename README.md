# mahalogin-master
# mahalogin-master
# mahalogin-master
# mahalogin-master
my First commit


================================================
My Jenkins Commands  and jfrog installation steps
=================================================
MFS088@DESKTOP-J5NRSS1 MINGW64 ~/Downloads (main)
$ ssh -i "MyJenkinsMasterKey7-9-2023.pem" ubuntu@ec2-18-191-218-79.us-east-2.compute.amazonaws.com

ubuntu@ip-172-31-3-171:~$ sudo -i
root@ip-172-31-3-171:~# apt-get update

root@ip-172-31-3-171:~# sudo apt-get install openjdk-8-jdk
root@ip-172-31-3-171:~# sudo apt-get install maven

root@ip-172-31-3-171:~# curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee \
>   /usr/share/keyrings/jenkins-keyring.asc > /dev/null
> 
root@ip-172-31-3-171:~# echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
>   https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
>   /etc/apt/sources.list.d/jenkins.list > /dev/null
> 
root@ip-172-31-3-171:~# sudo apt-get update

root@ip-172-31-3-171:~# sudo apt-get install jenkins

root@ip-172-31-3-171:~# sudo apt-get remove --purge jenkins

root@ip-172-31-3-171:~#  rm -rf /var/lib/jenkins

root@ip-172-31-3-171:~# ps -ef | grep jenkins
root        8519    1331  0 06:04 pts/0    00:00:00 grep --color=auto jenkins
root@ip-172-31-3-171:~# sudo kill -9 8519
kill: (8519): No such process
root@ip-172-31-3-171:~# sudo kill -9 1331
Killed
ubuntu@ip-172-31-3-171:~$ apt-get update

ubuntu@ip-172-31-3-171:~$ sudo service jenkins stop

ubuntu@ip-172-31-3-171:~$ sudo apt remove jenkins

ubuntu@ip-172-31-3-171:~$ sudo apt-get install openjdk-8-jdk

ubuntu@ip-172-31-3-171:~$ sudo apt-get install maven

ubuntu@ip-172-31-3-171:~$ curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee \
>   /usr/share/keyrings/jenkins-keyring.asc > /dev/null
ubuntu@ip-172-31-3-171:~$ echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
>   https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
>   /etc/apt/sources.list.d/jenkins.list > /dev/null
ubuntu@ip-172-31-3-171:~$ sudo apt-get install jenkins

ubuntu@ip-172-31-3-171:~$ git clone https://github.com/DikshaSTarte/mahalogin-master.git
Cloning into 'mahalogin-master'...
.
ubuntu@ip-172-31-3-171:~$ ls
mahalogin-master
ubuntu@ip-172-31-3-171:~$ cd mahalogin-master
ubuntu@ip-172-31-3-171:~/mahalogin-master$ ls
LICENSE  README.md  appgatewayurl.ps1  pom.xml  src


ubuntu@ip-172-31-3-171:~/mahalogin-master$ ls
LICENSE  README.md  appgatewayurl.ps1  pom.xml  src  target
ubuntu@ip-172-31-3-171:~/mahalogin-master$ cd
ubuntu@ip-172-31-3-171:~$ ls
mahalogin-master
ubuntu@ip-172-31-3-171:~$ ls -la
total 36
drwxr-xr-x 6 ubuntu ubuntu 4096 Sep  7 06:20 .
drwxr-xr-x 3 root   root   4096 Sep  7 05:52 ..
-rw-r--r-- 1 ubuntu ubuntu  220 Feb 25  2020 .bash_logout
-rw-r--r-- 1 ubuntu ubuntu 3771 Feb 25  2020 .bashrc
drwx------ 2 ubuntu ubuntu 4096 Sep  7 05:52 .cache
drwxrwxr-x 3 ubuntu ubuntu 4096 Sep  7 06:20 .m2
-rw-r--r-- 1 ubuntu ubuntu  807 Feb 25  2020 .profile
drwx------ 2 ubuntu ubuntu 4096 Sep  7 05:52 .ssh
-rw-r--r-- 1 ubuntu ubuntu    0 Sep  7 05:52 .sudo_as_admin_successful
drwxrwxr-x 5 ubuntu ubuntu 4096 Sep  7 06:20 mahalogin-master
ubuntu@ip-172-31-3-171:~$ cd .m2/
ubuntu@ip-172-31-3-171:~/.m2$ ls
repository
ubuntu@ip-172-31-3-171:~/.m2$ cd repository/
ubuntu@ip-172-31-3-171:~/.m2/repository$ ls
antlr        backport-util-concurrent  classworlds  commons-cli   commons-logging  dom4j  junit  mysql  xml-apis
aopalliance  ch                        com          commons-dbcp  commons-pool     javax  log4j  org    xpp3
ubuntu@ip-172-31-3-171:~/.m2/repository$ cd com/
ubuntu@ip-172-31-3-171:~/.m2/repository/com$ ls
fasterxml  google  maha  thoughtworks
ubuntu@ip-172-31-3-171:~/.m2/repository/com$ cd maha/
ubuntu@ip-172-31-3-171:~/.m2/repository/com/maha$ ls
mahaLogin
ubuntu@ip-172-31-3-171:~/.m2/repository/com/maha$ cd mahaLogin/
ubuntu@ip-172-31-3-171:~/.m2/repository/com/maha/mahaLogin$ ls
2.0  maven-metadata-local.xml
ubuntu@ip-172-31-3-171:~/.m2/repository/com/maha/mahaLogin$ cd 2.0/
ubuntu@ip-172-31-3-171:~/.m2/repository/com/maha/mahaLogin/2.0$ ls
_remote.repositories  mahaLogin-2.0.pom  mahaLogin-2.0.war

ubuntu@ip-172-31-3-171:~/.m2/repository/com/maha/mahaLogin/2.0$ sudo cat /var/lib/jenkins/secrets/initialAdminPassword
af200eeb81674ecaab106bf7ea4b4ca0

ubuntu@ip-172-31-3-171:~/.m2/repository/com/maha/mahaLogin/2.0$ cd /var/lib/jenkins
ubuntu@ip-172-31-3-171:/var/lib/jenkins$ ls
config.xml                                   jenkins.install.UpgradeWizard.state             nodes                     secrets
hudson.model.UpdateCenter.xml                jenkins.model.JenkinsLocationConfiguration.xml  plugins                   updates
hudson.plugins.git.GitTool.xml               jenkins.telemetry.Correlator.xml                queue.xml                 userContent
identity.key.enc                             jobs                                            secret.key                users
jenkins.install.InstallUtil.lastExecVersion  nodeMonitors.xml                                secret.key.not-so-secret  workspace
ubuntu@ip-172-31-3-171:/var/lib/jenkins$ cd workspace
ubuntu@ip-172-31-3-171:/var/lib/jenkins/workspace$ ls
MyFirstJenkinsJob
ubuntu@ip-172-31-3-171:/var/lib/jenkins/workspace$ cd MyFirstJenkinsJob
ubuntu@ip-172-31-3-171:/var/lib/jenkins/workspace/MyFirstJenkinsJob$ ls
LICENSE  README.md  appgatewayurl.ps1  pom.xml  src

--------------------------------------
for other job created a target folder at pom.xml file location and then mvn install perform 
------------------------
root@ip-172-31-3-171:/var/lib/jenkins/workspace/MySampleJob01# ls
LICENSE  README.md  appgatewayurl.ps1  pom.xml  src
root@ip-172-31-3-171:/var/lib/jenkins/workspace/MySampleJob01# mkdir target/
root@ip-172-31-3-171:/var/lib/jenkins/workspace/MySampleJob01# ls
LICENSE  README.md  appgatewayurl.ps1  pom.xml  src  target



root@ip-172-31-3-171:/var/lib/jenkins/workspace/MySampleJob01# ls
LICENSE  README.md  appgatewayurl.ps1  pom.xml  src  target
root@ip-172-31-3-171:/var/lib/jenkins/workspace/MySampleJob01# mvn install

[INFO] Installing /var/lib/jenkins/workspace/MySampleJob01/target/mahaLogin-2.0.war to /root/.m2/repository/com/maha/mahaLogin/2.0/mahaLogin-2.0.war
[INFO] Installing /var/lib/jenkins/workspace/MySampleJob01/pom.xml to /root/.m2/repository/com/maha/mahaLogin/2.0/mahaLogin-2.0.pom
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  16.740 s
[INFO] Finished at: 2023-09-07T07:41:57Z
[INFO] ------------------------------------------------------------------------
root@ip-172-31-3-171:/var/lib/jenkins/workspace/MySampleJob01# ls
LICENSE  README.md  appgatewayurl.ps1  pom.xml  src  target

root@ip-172-31-3-171:/var/lib/jenkins/workspace/MySampleJob01# cd target/
root@ip-172-31-3-171:/var/lib/jenkins/workspace/MySampleJob01/target# ls
classes  generated-sources  mahaLogin-2.0  mahaLogin-2.0.war  maven-archiver  maven-status
root@ip-172-31-3-171:/var/lib/jenkins/workspace/MySampleJob01/target#
