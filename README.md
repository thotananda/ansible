# Learn Ansible

#### Important Ansible Adhoc Commands
Ping all hosts 

``` ansible all -m ping ```

copy file from controller machine to traget machine

``` ansible all -m ansible.builtin.copy -a "src=/etc/hosts dest=/tmp/hosts"```

change file permissions on target machine

``` ansible webservers -m ansible.builtin.file -a "dest=/srv/foo/a.txt mode=600"```

change file permissions with users on target machine

```ansible webservers -m ansible.builtin.file -a "dest=/srv/foo/b.txt mode=600 owner=mdehaan group=mdehaan"```

create folder on target machine

``` ansible all -m ansible.builtin.file -a "dest=/tmp/nanda state=directory"```

delete folder on target machine

``` ansible all -m ansible.builtin.file -a "dest=/tmp/nanda state=absent"```

#### Managing packages

```ansible all -m ansible.builtin.yum -a "update_only=yes"```

```ansible all -m ansible.builtin.yum -a "name=python3 state=present"```

```ansible all -m ansible.builtin.yum -a "name=httpd state=absent" -u ec2-user --become``` # --become use for run as root user
