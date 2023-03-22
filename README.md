# ansible_tutorial

#Test de connexion au Hosts avec clé SSH:
ansible all --key-file ~/.ssh/ansible -i inventory -m ping

#Commande pour avoir des infos sur les serveurs
ansible all -i inventory -m gather_facts
