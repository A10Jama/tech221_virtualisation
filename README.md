# Virtualisation
## Virtual Machine: What is it?
A virtual machine (VM) is a computer system based on software that divides the resources of a physical machine among multiple virtual machines. Each VM runs its own operating system and applications in a separate environment to deploy, test, and run legacy applications.
![image](https://user-images.githubusercontent.com/129948378/232549051-823ea280-46e2-4774-81c2-a07400576d46.png)

## Development Environment: What is it?
A development environment is a setup that developers use to create and test software applications. It includes all the necessary tools, libraries, and configurations needed to create and run applications.
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
![image](https://user-images.githubusercontent.com/129948378/232556465-f0991550-f2ac-4076-809f-02701bb11cb3.png)

The four pillars of DevOps are:

-Effective communication
-Collaboration
-Automation
-Monitoring
These pillars promote cooperation, shared accountability, the use of tools and technology to speed up software delivery while reducing human error, and constant performance monitoring to find and fix problems as they arise.



