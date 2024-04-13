# Ansible-repo
This repo serves for learning purposes.

# 1- Inventory
First, add servers to the inventory (DNS or Static IP)
We'll get back and forth to the inventory later

# 2- Setting up SSH
Set ssh connexion between master node and the other servers
`ssh-keygen`

add local link to public key to the inventory
`ssh-copy-id -i PUBLIC_KEY DEST_SERVER`

# 3- ping test
ansible -i -m ping

