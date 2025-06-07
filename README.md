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
 2-  git clone https://github.com/ikambarov/Flaskex.git or ( git clone  https://github.com/anfederico/Flaskex.git )
 3-  cd Flaskex
 4-  curl -s https://bootstrap.pypa.io/pip/2.7/get-pip.py | python
 5-  pip install WTForms==2.3.3
 6-  pip install  -r  requirements.txt  try this if it doesnt work ( pip install  -r  Flaskex/requirements.txt )     
 7-  python app.py

#######

- pkill  -9  python =  it forcefully stops all running Python processes
- nohup python app.py = it keeps running even if your terminal is closed or you log out. (Normally, when you close your terminal or get disconnected (especially over SSH), running programs stop. 
  nohup prevents that.)
- nohup python app.py & = to run it in the background than add &
- netstat -plnt = This command lists network connections and listening ports on your system, showing useful details


# ansible-playbook  -i hosts  main.yml = testing playbook for playbook on vsc




####
NOTES..
2 rules while writing playbooks
- you cant automate something you dont know
- test one task at a time.
- create playbook before creating a role





















<img width="1502" alt="Screenshot 2025-06-06 at 12 57 08 PM" src="https://github.com/user-attachments/assets/334b1b8e-63d4-448a-9b37-5c89925a4a45" />








 
