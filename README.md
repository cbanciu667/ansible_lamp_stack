# ansible_lamp_stack

Deploy sample LAMP stack based on PHP 7, MYSQL 5.7 and NGINX 1.10 on Ubuntu 18.04 LTS
Step 1: install Ubuntu18 on a local virtualbox VM and give IP 192.168.0.111
Step 2: run converge command as per example bellow

usage example (run in playbook root): ansible-playbook -i inventory/local -c local ./deploy.yml

Prereq.: install sshpass, on MAC run brew install https://raw.githubusercontent.com/kadwanev/bigboybrew/master/Library/Formula/sshpass.rb
