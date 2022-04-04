# testing
to test my repo
## my first Ansible Playbook (YAML)
---
 -name: setup weservice
  hosts: websrv
  become: yes
  tasks:
        -name: Install httpd
         yum:
                name: httpd
                state: present
        -name: start & enable service
         service:
                name: httpd
                state: started
                enabled: yes
        -name: Copy file with owner and permissions
         copy:
                src: files/index.html
                dest: /var/www/html/index.html
                mode: '0644'
                backup: yes
 -name: setup db
 hosts: dbsrv
 become: yes
 tasks:
        -name: Install mysql
         yum:
                 name: mariadb-server
                 state: present
        -name: start & enable mydql
         service:
                name: mariadb
                state: started
                enabled: yes
