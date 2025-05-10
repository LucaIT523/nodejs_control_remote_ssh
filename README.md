# 

<div align="center">
   <h1>nodejs_control_remote_ssh</h1>
</div>



The SSHMng is designed to manage SSH connections and command execution using the node-ssh library. 

It supports both password-based and PEM private key-based login methods, includes timeout protection, and allows running commands remotely



### **1. SSH Manager Class (`SSHMng`)**

#### **Core Functionality**

​	Dual authentication: Password & PEM key,

​	Timeout-controlled connections (3s default),

​	Connection state tracking.



// Connection Methods

async connectServerPW() {}    // Password-based auth

async connectServerPEM() {}   // PEM key auth

async disconnectServer() {}   // Clean connection teardown



// Command Execution

async runCommand() {}         // Execute shell commands

async LoginAndRunCommand() {} // Full workflow: connect→execute→disconnect

async LoginPEMAndRunCommand() {}



**2. AutoCreateAndDelUser Function**


Connects to a remote server via SSH (using either password or PEM key).

Creates or resets a Linux user account.

Optionally regenerates SSH keys for the user.

Deletes old users when userOpt == "useradd".

Handles temporary usernames and passwords based on policy data.





This implementation demonstrates a robust SSH user management system suitable for enterprise environments requiring automated, policy-driven server access control. 

The combination of temporary credential support, comprehensive cleanup routines, and centralized credential storage makes it particularly suitable for secure, short-lived access scenarios.

### **Contact Us**

For any inquiries or questions, please contact us.

telegram : @topdev1012

email :  skymorning523@gmail.com

Teams :  https://teams.live.com/l/invite/FEA2FDDFSy11sfuegI