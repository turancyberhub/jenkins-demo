### First, create a file called ssh-key.pem and copy&paste EC2 private key from terraform repository

    touch ssh-key.pem
    vi ssh-key.pem

### Second, change the permission of the private key to ssh into ec2 instances

    chmod 400 ssh-key.pem

### Third, open inventory file and copy&paste private IP addresses from EC2 instances. For Jenkins, paste the private IP of the Jenkins server. For k8s, paste the private IP of the Kubernetes server
    
    vi inventory 
    k8s ansible_host=<Private IP>


### Finally, run the ansible commands one by one 

    ansible-playbook install-k8s.yml -i inventory



Note: Installation might take sometime, please wait till the end. 
