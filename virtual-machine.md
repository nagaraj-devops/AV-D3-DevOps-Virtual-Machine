## What is a Server?
- A server is basically a computer system or program that provides services, data, or resources to other computers (called clients) over a network.

### Types of Servers

1. Web Server – Serves web pages (e.g., Nginx, Apache).
2. Database Server – Stores and manages data (e.g., MySQL, PostgreSQL).
3. File Server – Stores and shares files across a network.
4. Application Server – Hosts and runs applications.
5. Mail Server – Sends and receives emails (e.g., Postfix, Microsoft Exchange).
6. DNS Server – Translates domain names (like google.com) into IP addresses.

  
## Pysical vs Virtual

⚡ Physical Server

Definition: A dedicated, standalone hardware machine that runs server software.

Resources: CPU, RAM, storage, and network are fixed to that machine.

Example: A Dell PowerEdge rack server running only one OS (like Windows Server or Linux).

✅ Pros:

High performance (dedicated hardware).

Full control over resources.

More secure (isolated, not shared).

❌ Cons:

Expensive (hardware, maintenance, power, cooling).

Less flexible (hard to scale).

Single point of failure (if hardware fails, downtime occurs).

----------------------------------------------------------------------------------------------------
⚡ Virtual Server

Definition: A server created using virtualization software (like VMware, Hyper-V, KVM) inside a physical machine.

One physical server can run multiple virtual servers (VMs).

Each VM acts like a separate server with its own OS and apps.

✅ Pros:

Cost-effective (multiple servers on one machine).

Easy to scale and manage.

Better resource utilization.

High availability (can move VMs between hosts).

❌ Cons:

Slight performance overhead (since hardware is shared).

Depends on the physical host (if the host crashes, all VMs go down unless redundancy is set up).

Security risks if not properly isolated.

| Feature     | Physical Server              | Virtual Server                         |
| ----------- | ---------------------------- | -------------------------------------- |
| Hardware    | Dedicated machine            | Shared (runs on a physical host)       |
| Scalability | Hard (requires new hardware) | Easy (create new VMs quickly)          |
| Cost        | High                         | Low                                    |
| Performance | Maximum (dedicated)          | Slightly lower (shared)                |
| Maintenance | Hardware + software          | Mostly software (less hardware hassle) |

## Hypervisor
- A Hypervisor is the software or firmware layer that allows you to run multiple virtual servers (VMs) on a single physical server.
  - ### What is a Hypervisor?
    - It sits between the hardware and the virtual machines.
    - It manages and allocates CPU, memory, storage, and network resources to each VM.
    - Each VM behaves like an independent computer with its own OS and apps.
  - ### Types of Hypervisors
    1. Type 1 (Bare-Metal Hypervisor)
       - Installed directly on the hardware.
       - More efficient, used in data centers.
       - Examples: VMware ESXi, Microsoft Hyper-V, KVM, Xen.

    2. Type 2 (Hosted Hypervisor)
      - Runs on top of an existing operating system.
      - Easier to use for testing and development.
      - Examples: VMware Workstation, Oracle VirtualBox, Parallels Desktop.

Example
- Imagine a physical server with:
- 32 GB RAM, 16 CPUs, 1 TB storage.

### A hypervisor can divide it into:
1. VM1 → 8 GB RAM, 4 CPUs, Ubuntu.
2. VM2 → 16 GB RAM, 6 CPUs, Windows Server.
3. VM3 → 8 GB RAM, 6 CPUs, CentOS.

* All running independently on the same hardware. *


## How to create VM?

🖥️ 1. Create a VM Locally (Using a Hypervisor)

You’ll need a Type-2 Hypervisor like VirtualBox or VMware Workstation.

🔹 Steps with VirtualBox (example):

- Install VirtualBox.
- Open VirtualBox.
- Name your VM → Select OS type (Windows/Linux).
- Allocate RAM (e.g., 4 GB).
- Create Virtual Hard Disk (e.g., 50 GB).
- Attach ISO Image (Ubuntu ISO, Windows ISO, etc.).
- Start VM → It will boot from the ISO and install OS.
- Done ✅ You have a running VM.

☁️ 2. Create a VM in Cloud (AWS EC2 example)

- Log in to AWS Console.
- Go to EC2 → Launch Instance.
- Choose AMI (Amazon Machine Image) → e.g., Ubuntu, Windows.
- Select Instance Type (e.g., t2.micro = 1 vCPU, 1 GB RAM).
- Configure Storage & Security Groups (allow SSH/HTTP).
- Launch Instance → Download the key pair (.pem).
- Connect to VM via SSH: ssh -i key.pem ubuntu@<public-ip>
- Now you have a VM running in the cloud.
