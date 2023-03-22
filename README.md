# ansible_tutorial

#Test de connexion au Hosts avec clé SSH
ansible all --key-file ~/.ssh/ansible -i inventory -m ping
