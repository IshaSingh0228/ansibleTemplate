 Using Common inventory
 
 ansible-playbook -i ~/inventory.ini -u ubuntu nginx_playbook.yml --private-key ~/awskeypair.pem

 Also had to change file permissions of the key (was initially 664) through 

 sudo chmod 600 ~/awskeypair.pem

 $ls -la shows file permissions

 Some Commands :

 sudo service nginx status
  sudo service nginx start
   sudo service nginx stop