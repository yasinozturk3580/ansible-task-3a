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
 1 -  yum install git -y
 2 -  git clone https://github.com/ikambarov/Flaskex.git or ( git clone  https://github.com/anfederico/Flaskex.git )
 3 -  cd Flaskex
 4 -  curl -s https://bootstrap.pypa.io/pip/2.7/get-pip.py | python
 5 -  pip install WTForms==2.3.3
 6 -  pip install  -r  requirements.txt  try this if it doesnt work ( pip install  -r  Flaskex/requirements.txt )     
 7 -  python app.py
 8 -  ss -tulnp | grep :5000 =  it shows details about any process using TCP/UDP port 5000
 9 -  kill -9 = its used to forcefully terminate a process using its PID (Process ID) Example = kill -9   59543   59525
 10 - pkill -f app.py = This will automatically stop that process — even if it’s running in the background or with nohup
     Caution: 
  It will kill all processes matching app.py in the command line.
  Use carefully if you have more than one script with similar names.

11- pkill  -9  python =  it forcefully stops all running Python processes
12- nohup python app.py = it keeps running even if your terminal is closed or you log out. (Normally, when you close your terminal or get disconnected (especially over SSH), running programs stop. 
  nohup prevents that.)
13- nohup python app.py & = to run it in the background than add &
14- netstat -plnt = This command lists network connections and listening ports on your system, showing useful details
15- ss -plnt =  This command lists network connections and listening ports on your system, showing useful details

####
# with VSC playbook.
1- create main.yml file under ansible-task-3a
2- create hosts file
after playbook 
3- create roles folder under ansible-task-3a
run this commands in roles folder = A - ansible-galaxy  init  git-role 
B- ansible-galaxy  init  pip-role
4- rm -rf git-role/
5- rm -rf pip-role/
6- ansible-galaxy  init  ansible-git-role
7- ansible-galaxy  init  ansible-pip-role
- keep files defaults,meta,tasks,readme  delete rest of them.



#  ansible  -i hosts  all  -m ping
#  ansible-playbook  -i hosts  main.yml = testing playbook for playbook on vsc
# rm -rf ( file or folder name ) : delete it



####
NOTES..
2 rules while writing playbooks
- you cant automate something you dont know
- test one task at a time.
- create playbook before creating a role






























<img width="1506" alt="Screenshot 2025-06-06 at 9 57 28 PM" src="https://github.com/user-attachments/assets/b2b7b40b-a816-4a4d-94e4-79b37dd20b1e" />


 
