# 🍺 Full service node setup guide

# Prerequisites:

Hardware and Operating System: You'll need a VPS (Virtual Private Server) or a dedicated server with sufficient resources (CPU, RAM, and storage). Popular choices include Ubuntu 18.04 or 20.04 LTS for the operating system.

**Sispop Collateral:** You'll need the required amount of Sispop as collateral for your Service Node. The exact amount may vary, so check the official documentation for the latest requirements. Curently the required Collateral Amount is **147459.949759196**. You can also
referred to the official explorer page and see **The staking requirements**. The explorer is [Sispop Explorer](https://explorer.sispop.site/)

**Sispop Wallet:** You should have a Sispop wallet set up and funded with the necessary collateral. The official Sispop wallet is recommended. The official sispop wallet can be downloaded from [https://github.com/sispop-dev/sispop/releases](https://github.com/sispop-dev/sispop/releases).

# Step-by-Step Setup

**Server Setup:**

Create a VPS or dedicated server instance with the chosen operating system.
Secure your server by configuring firewalls, SSH keys, and regular system updates.

Install Dependencies **(If self compiling)**:

# SSH into your server .
Install required dependencies such as Git, CMake, and build tools  **(If self compiling)**.
Refer to the official documentation for specific installation commands for your OS.
####  Firewall Configuration

If you are using a firewall then ensure that the following ports are open/reachable

* Port 22020 (storage server to storage server)
* Port 22021 (client to storage server)
* Port 20000 (blockchain syncing)
* Port 50000 (Service Node to Service Node)
* Port 1090 (UDP, not TCP, unlike all of the above; Sispopnet router data)

# Download Sispop Repository:

Clone the Sispop repository from GitHub to your server using Git.
Navigate to the repository directory.
Build the Sispop Software:

Use the CMake and make tools to build the Sispop software.
This step will compile the Sispop software on your server.

## Initialize the Service Node and Configuration:

Initialize your Service Node by running the appropriate command. This process will set up your Service Node and configure it with the collateral you provided. Use the sispopd daemon with the below command.

```java
./sispopd --service-node --service-node-public-ip 180.23.44.5XX --storage-server-port 22020
```
Be sure to follow the instructions carefully and make sure to change 180.23.44.5XX to your own vps ip address.

Once the daemon is running put the following command:

```java
prepare_registration
```
and once you do that, the below prompt will be displayed as follow:

```java
Current staking requirement: 147451.811839611 sispop
Will the operator contribute the entire stake? (Y/Yes/N/No/C/Cancel):
```
if you want others to also contribute put no as shown below:

```java
Will the operator contribute the entire stake? (Y/Yes/N/No/C/Cancel): n
Enter operator fee as a percentage of the total staking reward [0-100]% (B/Back/C/Cancel): 80
Do you want to reserve portions of the stake for other specific contributors? (Y/Yes/N/No/B/Back/C/Cancel): y
Number of additional contributors [1-3] (B/Back/C/Cancel): 3
```
The next step is to enter the address that you want to use for the service node and the address that will receive the **1650 SISPOP**

```java
Enter the sispop address for the operator (B/Back/C/Cancel): 43....your-address...
```
Once you tap enter it would output some thing like the below code

```java
register_service_node 4294967292 49g7Layd4PyDYTh76txXvNEQ7VwV3wDUc28ZipomrKeGWiaYgQenqExDEdga3cgmAiWz86DYDzPZxeL947SxE9caN22NP7g 4294967292 100.000000000 1535677391 ec3895ea70a4a91b5ec4b5e1df96a45e07046f1fb0123c754d98fb2d70f4529d 5bb35d7b8ab1acb943bc47913ada8f9d2e6d6e22264e57484a04c1bbfd461f0ee2e5435454cd9b7059b221eb506ce9ea4537ddd9faf1f1757e0ef611a41c0609
```
the above code would be put in your **sispop-wallet-cli** or Use your electron GUI wallet and once you do that it would register your service node and you will earn **1650 SISPOP** per block.


## Monitor and Maintain:

Regularly check the status of your Service Node to ensure it's online and working correctly.
Keep your server and Sispopsoftware up to date by following the project's updates.
Backup and Security:

Implement backup and security measures to protect your Service Node and collateral.

Join the Sispop Network:

Once your Service Node is up and running, you can register it on the Sispop network to start participating in the Service Node quorums.
