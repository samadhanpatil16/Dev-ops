# Dev-ops Asible training

-------Ansible -------------------------------------------------------------------------------------------
#Install ansible- command-  python needed
 sudo yum install python3-pip - python
 sudo pip3 install ansible/  - ansible 
----------------------------------------------
# ansible --version
#  whereis ansible
cd  /etc/ansible - create if not-  it's defult dir of ansible
#crete dir- all support file
/home/ec2-user/ansible -  inventory file, config file
1. ansible.cfg   -.cfg
2.hosts  -txtfile- invenntory file
#Command:
ansible-playbook playbook.yml --syntax-check

ansible-playbook playbook.yml
ansible-playbook playbook.yml --step
--------------install java--------------------------------------
sudo yum install java-1.8*
sudo yum install git -y
sudo yum install wget unzip -y 
------------in mven---------------------------------------
#install mvn
wget https://downloads.apache.org/maven/maven-3/3.6.3/binaries/apache-maven-3.6.3-bin.tar.gz
extrat zip and move below path
mv <extract dir> /opt/maven
#set  mven path #home path
cd ~
ln -s /opt/maven/bin/mvn  /usr/bin/mvn

------------------------------------
#install jenkin- go zenkin site
https://pkg.jenkins.io/redhat-stable/
#command
sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key
#enable jenkins  service #3a6190584cef4155ba4b4126e5c8612e =pwd
   systemctl status jenkins
   sudo systemctl start jenkins
   sudo systemctl enable jenkins
--------------------------------------
go to tomcat site
 
 wget <tar file url of tomcat>
 extract tar file
 move extract dir to /opt/tomcat
 
 sh /opt/tomcat/bin/shutdown.sh &
 sh /opt/tomcat/bin/startup.sh &
------------------------------------------------------

#enable ssh root login in ssh cofig file
   vi /etc/ssh/sshd_config - enable pwd authentication=yes
#restart sshd service 
  systemctl restart sshd
    
#change password of ec2-user(pwd=admin)
sudo su
passwd <ec2-user>

#--------genearte key---------------------------------------
 ssh-keygen  
#copy key to retome server 
 ssh-copy-id usr@<severname> 
