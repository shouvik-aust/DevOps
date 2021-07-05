# Class 1

## Network Interface
A network interface is the point of interconnection between a computer and a private or public network. A network interface is generally a network interface card (NIC), but does not have to have a physical form. Instead, the network interface can be implemented in software.

**It fetches packets from Hardware to Kernel.**

## User space
It refers to all of the code in an operating system that lives outside of the kernel. Most Unix-like operating systems (including Linux) come pre-packaged with all kinds of utilities, programming languages, and graphical tools - these are user space applications.

## Kernel
It is the core component of an operating system. Using interprocess communication and system calls, it acts as a bridge between applications and the data processing performed at the hardware level. When an operating system is loaded into memory, the kernel loads first and remains in memory until the operating system is shut down again. The kernel is responsible for low-level tasks such as disk management, task management and memory management.

*Any software is a **process**, any process performs some system calls.*

## DHCP
The Dynamic Host Configuration Protocol (DHCP) is a network management protocol used on Internet Protocol (IP) networks for automatically assigning IP addresses and other communication parameters to devices connected to the network using a client–server architecture.

## What Is a Cam Table?
CAM table allows information routed through the switch to be addressed to a single computer on the network, rather than to all networked computers. This increases the specificity of information traveling through the network, at the cost of an increase in vulnerability to network system hacking attempts.

## Docker
Docker is an open source containerization platform. It enables developers to package applications into containers—standardized executable components combining application source code with the operating system (OS) libraries and dependencies required to run that code in any environment.

*Docker isn't a replacement of VM, rather it's an way to utilize VM. Thery are used parallely in current industry.*

## Cloud computing
The delivery of on-demand computing services -- from applications to storage and processing power -- typically over the internet and on a pay-as-you-go basis.
*Combination of Infrastructure, SND & SDS.*

## KVM
Kernel-based Virtual Machine (KVM) is an open source virtualization technology built into Linux®. Specifically, KVM lets you turn Linux into a hypervisor that allows a host machine to run multiple, isolated virtual environments called guests or virtual machines (VMs).

## Virtual private cloud
A virtual private cloud (VPC) is a secure, isolated private cloud hosted within a public cloud. VPC customers can run code, store data, host websites, and do anything else they could do in an ordinary private cloud, but the private cloud is hosted remotely by a public cloud provider. 
![image](https://user-images.githubusercontent.com/25537164/124511941-1131be80-ddf9-11eb-9b2c-f34bdbe39571.png)

## Container
A container is a standard unit of software that packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another.

*Container is a process.*

## Hypervisor
A hypervisor is software that creates and runs virtual machines (VMs). A hypervisor, sometimes called a virtual machine monitor (VMM), isolates the hypervisor operating system and resources from the virtual machines and enables the creation and management of those VMs. The physical hardware, when used as a hypervisor, is called the host, while the many VMs that use its resources are guests. The hypervisor treats resources—like CPU, memory, and storage—as a pool that can be easily reallocated between existing guests or to new virtual machines.

## Container vs Hypervisor
![image](https://user-images.githubusercontent.com/25537164/124512202-a0d76d00-ddf9-11eb-8a49-fe2fcfd548e1.png)

***DD = docker daemon***

*Hypervisor is Hardware dependent, Docker is Software dependent*

## Building a Docker Container
![image](https://user-images.githubusercontent.com/25537164/124512617-a08ba180-ddfa-11eb-892a-5375c716cf2c.png)


### Format of the Dockerfile:
`INSTRUCTION arguments`

**Docker File Example:**
`FROM ubuntu`
`CMD ["Sleep", "300"]`

### Build a Docker Image:
1. `sudo docker build -t [name/path] .`: builds the docker file 
2. `sudo docker run -p [port]:[port] [name/path]` : runs the docker file & creates a container, *The container shall start to run* 
3. `sudo ps` : checks the running container info
4. `docker exec -it [container_id] sh` : execute an interactive bash shell on the container (optional)
