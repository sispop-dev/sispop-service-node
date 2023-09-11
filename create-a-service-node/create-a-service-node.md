# 🍺 Full service node setup guide

# Prerequisites:

Hardware and Operating System: You'll need a VPS (Virtual Private Server) or a dedicated server with sufficient resources (CPU, RAM, and storage). Popular choices include Ubuntu 18.04 or 20.04 LTS for the operating system.

**Sispop Collateral:** You'll need the required amount of Sispop as collateral for your Service Node. The exact amount may vary, so check the official documentation for the latest requirements.

**Sispop Wallet:** You should have an Sispop wallet set up and funded with the necessary collateral. The official Sispop wallet is recommended.

# Step-by-Step Setup

**Server Setup:**

Create a VPS or dedicated server instance with the chosen operating system.
Secure your server by configuring firewalls, SSH keys, and regular system updates.
Install Dependencies:

## SSH into your server.
Install required dependencies such as Git, CMake, and build tools.
Refer to the official documentation for specific installation commands for your OS.
Download Sispop Repository:

Clone the Sispop repository from GitHub to your server using Git.
Navigate to the repository directory.
Build the Sispop Software:

Use the CMake and make tools to build the Sispop software.
This step will compile the Sispop software on your server.
Initialize the Service Node:

Initialize your Service Node by running the appropriate command. This process will set up your Service Node and configure it with the collateral you provided.
Be sure to follow the instructions carefully, as they may include generating a Service Node key pair.

## Configuration:

Configure your Service Node by editing the node configuration file. This file contains various settings, including your Sispop wallet address and other options.
Ensure your Service Node is correctly configured to connect to the Sispop network.

## Start the Service Node:

Start your Sispop Service Node by running the appropriate command.
Monitor the logs to ensure everything is running smoothly.

## Monitor and Maintain:

Regularly check the status of your Service Node to ensure it's online and working correctly.
Keep your server and Sispopsoftware up to date by following the project's updates.
Backup and Security:

Implement backup and security measures to protect your Service Node and collateral.

Join the Sispop Network:

Once your Service Node is up and running, you can register it on the Sispop network to start participating in the Service Node quorums.
