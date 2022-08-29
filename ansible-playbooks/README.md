### Usage
Just run the command and everything will be settled.
```
ansible-playbook install.yml -i inventory --extra-vars "target_host=127.0.0.1 ansible_port=22"  --extra-vars "ansible_user=user ansible_password=password"
```
### Tips
If ones want to test the script with docker, you can refer my steps:
```
sudo docker run -e ROOT_PASSWORD=root -p  127.0.0.1:8022:22 -it takeyamajp/ubuntu-sshd:ubuntu20.04
```
and
```
ansible-playbook install.yml -i inventory --extra-vars "target_host=127.0.0.1 ansible_port=8022"  --extra-vars "ansible_user=root ansible_password=root"
```
After everything are installed. SSH into the docker to check if everything is ok.
```
ssh root@localhost -p 8022
```
