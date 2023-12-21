---
- hosts: webservers
  become: True
  tasks:
    - name: Install packages
      yum:
        name: "nginx"
        state: "present"
    - name: Start Nginx Server
      service:
        name: nginx
        state: started
        enable: True
    - name: Deploy static website
      copy:
        src: index.html
        dest: /usr/share/nginx/html/
...
