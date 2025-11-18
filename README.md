# ITD_K8S_install_Scrpt
installation guide 




Kubeadm Setup

Click: Setup Script
STEP1:  Create a master 

Create an ec2 with t2.medium type and run the below command 
curl -s <github_script_raw_url> | bash -s master 
if the above command executes successfully then we get kubeadm join command with the token save this command in a separate file, and run this join command in worker nodes to add to this master. 
STEP2: Add worker nodes 

Create 2 ec2 with t2.micro type and run the below command 
curl -s <github_script_raw_url> | bash -s worker 
Run the kubeadm join command which we got from a master node in worker nodes to add to that master. 
(If the join command is lost run this in the master node: kubeadm token create --print-join-command)


<img width="1223" height="99" alt="image" src="https://github.com/user-attachments/assets/10479253-7b52-4ca0-bf5d-1941735a6989" />

