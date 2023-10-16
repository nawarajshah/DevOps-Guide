# This page will explain how to setup what you need to setup.

## How to setup local kuberenetes cluster?

1. Install Docker
2. [Install Virtualbox](install_virtualbox.md)
3. Install minikube
4. Install kubectl
5. [Install helm](instal-helm.md)


## How to setup basic monitoring in cloud?

## How to Setup your personal cloud?

## How to access AWS EC2?

### 1.  Setup an AWS Account:
* Go to [AWS homepage](https://aws.amazon.com/).
* Click on “Create an AWS Account” and fill in the necessary information.

### 2. Access AWS Management Console:
* After setting up the account, log in to the AWS Management Console.

### 3. Navigate to EC2 Dashboard:
* In the AWS Management Console, search for or select "EC2" to go to the EC2 Dashboard.

### 4. Launch Instance:
* Click on “Launch Instance” to create a new virtual machine.
* You’ll be prompted to choose an Amazon Machine Image (AMI), which is a template for the root volume for the instance.

### 5. Choose an Instance Type:
* Select the hardware configuration for your instance.
* Click “Next” to configure instance details.

### 6. Configure Instance:
* Specify the number of instances, purchasing option, network settings, and additional configurations.
* Click “Next” to add storage.

### 7. Add Storage:
* You can modify the storage settings or leave them as default.
* Click “Next” to add tags.

### 8. Add Tags:
* Create tags to manage your instances.
* Click “Next” to configure the security group.

### 9. Configure Security Group:
* Set up a security group, a virtual firewall, to control inbound and outbound traffic.
* Click “Review and Launch.”

### 10. Review:
* Verify your instance configurations.
* Click “Launch.”

### 11. Key Pair:
* A pop-up window will appear asking you to create a new key pair or use an existing one.
* Download the key pair and keep it secure, as this is needed to connect to your instance.

### 12. Access the EC2 Instance:
* Once the instance is launched, you can connect to it.
* Select the instance from the EC2 Dashboard and click “Connect” to get connection instructions.

### 13. SSH into Your Instance (for Linux instances):
* Use an SSH client with the downloaded key pair to connect to the instance. Example command:
~~~
ssh -i "your-key-pair.pem" ec2-user@your-instance-public-dns
~~~
* Make sure to replace "your-key-pair.pem" with your actual key pair file name and "your-instance-public-dns" with your actual instance's public DNS.

### 14. RDP into Your Instance (for Windows instances):
* You can use Remote Desktop Protocol (RDP) with the administrator password to connect to the instance.

## How to setup ssh and clone github repository through ssh?

1. Create ssh - key
``` ssh-keygen -t rsa ```
2. copy the generated RSA content to ssh settings in github dashboard.
3. eval `ssh-agent`
4. ssh-add <your-rsa-file-name>
