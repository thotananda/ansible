## Description
Copying local files to remote location

backup copied files on remote location if any changes happend

## Ping Servers
ansible all -i hosts -m ping -u root --ask-pass

## Run Playbook
ansible-playbook -i hosts playbook.yaml -u root --ask-pass
