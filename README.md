# ansible-task-3a
solution for task-3a

# Ansible Task 1 - install Flaskex Python application:

-  Clone https://github.com/ikambarov/Flaskex.git
-  Install the app on CentOS VM
-  Make sure web site is accessible at public IP over port 5000

- Ansible Playbook should be idempotent

Use
 -   handlers
 -   variables
 -    conditionals
 -    roles

# create github repository name is ansible-task-3a 
1- git clone repository in ansible VM  (  git clone git@github.com:yasinozturk3580/ansible-task-3a.git )
2- go to vsc open the folder ( ansible-task-3a )
3- create centos vm for task on droplets
4- first do the task manually on vm

# manually solution
 # create vm1 on droplets
 1-  yum install git -y
 2-  git clone https://github.com/ikambarov/Flaskex
 3-  cd Flaskex
 4-  curl -s https://bootstrap.pypa.io/pip/2.7/get-pip.py | python
 5-  pip install WTForms==2.3.3
 6-  pip install  -r  requirements.txt  try this if its doesnt work ( pip install  -r  Flaskex/requirements.txt )     
 7-  python app.py
