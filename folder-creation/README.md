## Description
create sample folder/directory on remote machine

## Ping Servers
ansible all -i hosts -m ping -u root --ask-pass

## Run Playbook
ansible-playbook -i hosts playbook.yaml -u root --ask-pass
