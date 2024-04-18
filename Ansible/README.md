# Ansible-repo
This repo serves for learning purposes.

# 1- Inventory
First, add servers to the inventory (DNS or Static IP)
We'll get back and forth to the inventory later

# 2- Setting up SSH
Set ssh connexion between master node and the other servers
`ssh-keygen`

add local link to public key to the inventory (do that to all servers)
`ssh-copy-id -i PUBLIC_KEY DEST_SERVER` 

# 3- ping test
ansible all -m ping

# 4- monitoring
`ansible all -m gather_facts`
can add `--limit DEST_SERVER` for tailoring the research

# note
web_servers:
- 10.10.10.101 (ubuntu)
- 10.10.10.151 (centos)

db_servers:
- 10.10.10.102 (ubuntu)
- 10.10.10.151 (CentOS)

file_servers:
- 10.10.10.103 (ubuntu)

# execute the playbooks
Execute the whole yml file : `ansible-playbook --ask-become-pass install_apache.yml`
Execute with tag(s) : `ansible-playbook --tags "mariadb,ubuntu" --ask-become-pass site.yml` note: no space allowed between the tags.
List the tags of a yml file : `ansible-playbook --list-tags site.yml`


