# ansible_tutorial

#Test de connexion au Hosts avec clé SSH:
ansible all --key-file ~/.ssh/ansible -i inventory -m ping

#Commande pour avoir des infos sur les serveurs
ansible all -i inventory -m gather_facts
ansible all -i inventory -m apt -a update_cache=true --become --ask-become-pass
ansible all -i inventory -m apt -a name=snapd --become --ask-become-pass
ansible all -i inventory -m apt -a name=snapd state=latest  --become --ask-become-pass
ansible all -i inventory -m apt -a upgrade=dist --become --ask-become-pass
ansible-playbook -i inventory --ask-become-pass install_apache.yml
