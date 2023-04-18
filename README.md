# Virtualisation
## Virtual Machine: What is it?
A virtual machine (VM) is a computer system based on software that divides the resources of a physical machine among multiple virtual machines. Each VM runs its own operating system and applications in a separate environment to deploy, test, and run legacy applications.
![image](https://user-images.githubusercontent.com/129948378/232549051-823ea280-46e2-4774-81c2-a07400576d46.png)

## Development Environment: What is it?
A development environment is a setup so that developers can create and test software applications. It includes all the necessary tools, libraries, and configurations needed to create and run applications.
![image](https://user-images.githubusercontent.com/129948378/232550428-98e26852-7520-4c12-8c71-484b18acf6d3.png)

## The Purpose of Creating a Development Environment
A development environment is created to provide developers with a workspace where they can create, test and debug their software applications. It ensures that the software developed is error-free, efficient, and meets the required standards.
# Vagrant
Vagrant is an open-source software tool that helps to manage and provision virtual machines (VMs) for software development. It allows developers to easily create and configure lightweight, portable, and reproducible development environments, which can be used to run their applications.

![image](https://user-images.githubusercontent.com/129948378/232552164-aa93bf3b-52b8-44d7-a928-e8a15625ba5f.png)

## Vagrant Command List
check above files for command list
https://github.com/A10Jama/tech221_virtualisation/blob/main/Vagrant_Commands.md
## Vagrant VirtualBox Connection

To connect to VirtualBox using Vagrant, follow these steps:

- Install VirtualBox and Vagrant.
- Create a new directory for the Vagrant project using the `mkdir <filename>` command in Git Bash.
- Open Git Bash terminal and navigate to the created directory using `cd` and `ls`.
- Initialize a new Vagrant project using `vagrant init`.
- Edit the Vagrantfile, changing the commented lines and setting `base` to `ubuntu` if you want to use Ubuntu.
- Save the Vagrantfile and turn on autosave for future reference.
- Start the VM by running `vagrant up`.
- To SSH into the VM, run `vagrant ssh` in another terminal session.
- Use "vagrant halt" to shut down the VM and `vagrant destroy` to delete the VM.

## The 4 Pillars of DevOps

### Cost
The goal of DevOps is to optimise the delivery of software by streamlining processes, increasing efficiency, and reducing waste. This includes reducing the cost of developing and maintaining software by implementing automation, reducing manual work, and improving collaboration and communication between teams.

### Flexibility 
Flexibility is a key aspect of DevOps because it allows teams to deliver software quickly, respond to changing customer needs, and keep up with the pace of technological change. 

### Ease of use 
DevOps tools that are easy to use and have a simple, intuitive interface can help reduce the learning curve for team members, making it easier for them to adopt and use the tools effectively.

### Robustness
Robustness in DevOps refers to the stability and reliability of software systems under different conditions. It is achieved through continuous testing, monitoring, feedback, and building redundancy and fault tolerance into systems.


## The Elements of a good dev enviroment 

A good development environment should have the following elements:

Simple updates and user-friendly interfaces to increase productivity and efficiency
Consistency to avoid unexpected errors, security vulnerabilities, or performance issues
Manageability to reduce complexity and clutter
Access to the same tools and resources for everyone regardless of location or device

# Vagrant Provisioning
<img width="862" alt="Screenshot 2023-04-17 at 16 53 08" src="https://user-images.githubusercontent.com/129948378/232561769-19f87075-3c3c-45f6-a6d5-f96340c13784.png">

1. IF VM is halted, `vagrant halt`, we create our shell script using `touch provision.sh`.
2. We use `nano provision.sh` to edit the contents and we enter the code in the following format:

    * `sudo apt-get update -y`
    * `sudo apt-get upgrade -y`
    * `sudo apt-get install -y`
    * `sudo apt-get install nginx`
    * `systemctl status nginx`
    
3. We now change permissions by using `chmod -x provision.sh` this will make it executable
4. We now move over to VScode, our vagrant file we created in the Vagrant Virtualbox connection, we will now add another line to utilise this shell script on launch: `config.vm.provision :shell, path: "provision.sh"`.
5. Going back to our terminal, we use the command `vagrant up`. We can now `vagrant ssh` into the VM, on top of this, grab the ip address from the vagrant file we updated, and copy and paste the ip in the search bar. 
<img width="865" alt="Screenshot 2023-04-17 at 16 52 31" src="https://user-images.githubusercontent.com/129948378/232561928-f7412839-2f8c-4036-a3cc-824d1b1c4289.png">

Your IP address should now work with nginx 
<img width="862" alt="Screenshot 2023-04-17 at 18 22 49" src="https://user-images.githubusercontent.com/129948378/232562276-01370590-987d-49eb-88da-1ce1fcd4ea32.png">
