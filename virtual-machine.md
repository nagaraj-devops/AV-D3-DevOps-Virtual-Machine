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

## How to create VM?

## Real World example
