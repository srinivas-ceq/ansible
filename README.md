# ansible
Ansible_playbook Sample


 # Master _EC2_Stepts #

# Stept_1
change hostname :   hostnamectl set-hostname  <newname>

# Stepet_2

update the server : sudo apt update

# Stept _3
set the following stepts 
sudo apt install software-properties-common
sudo apt-add-repository ppa:ansible/ansible

# Stept-_4
sudo apt install ansible
check the ansible --version
# Stept _5

genaraete the SSH_KEYGEN

# Stept _6
send a our pem file to master server using with winscp tool  defualt location /home/ubuntu/ 

above pem file copy the pem file  from /home/ubuntu/.pem to /etc/ansible/.pem 

 # Stept _7

set the IP's in  hosts file  Master and Node1 IP's note in hosts file

# Stept_8 
 check the ssh connection  ansible -m ping all using ping module 

# Stept _9

if you get erros in ssh connects  you can chnage the sudo user in  ansible.cfg  in defalt section remove # at sudo user line

# Stept _10 

now add the our pem key to ansible  following command 

ansible -m ping -u ubuntu --private-key=ansb.pem all

now it will ssh connection sucess.

# Stept_11

now change the name in hosts file 
server ip ansible_user=ubuntu
node ip ansible_user=ubuntu
ands run the command with out user like a .. ansible -m ping --private-key=ansb.pem all 
 
 # Stept_12
Execute the playbook
 ansible-playbook myplaybook.yml


 # Node_EC2_Stept #


# Stept_1
cahnge hostname :   hostnamectl set-hostname  <newname>

# Stepet_2

update the server : sudo apt update

# Stept _3
set the following stepts 
sudo apt install software-properties-common


# Stept-_4
sudo apt install nginx
check the ansible --version

 
