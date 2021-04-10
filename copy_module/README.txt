sudo ansible -i inventory.ini -u ubuntu -m ping all --private-key ~/awskeypair.pem

sudo ansible-playbook -i inventory.ini -u ubuntu copy_playbook.yml --private-key ~/awskeypair.pem