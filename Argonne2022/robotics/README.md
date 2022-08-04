# Environment description to control/manage Opentrons using the Docker container
Prerequisites: Basic Linux experience, familiarity with single-board computers like a Raspberry Pi, and a basic skill of Docker/ROS.

### Table of contents:
1. Hardware needed
2. Enabling root SSH access
3. Establishing connection
4. Run Python code

### Hardware needed
- OT-2[^1] Robot and Pipettes
- Nvidia Jetson Nano installed and attached [JetPack 4.1.1 SD card image](https://developer.nvidia.com/embedded/jetpack-sdk-441-archive)

### Enabling root SSH access
1. Install third-party tools as a first step: ```cURL``` and ```OepnSSH``` (Note. both might be installed by default on Linux.)
2. Generate a key pair: (1) Run ssh-keygen ```ssh-keygen -f ot2_ssh_key``` and press enter,

2. Enter a passphrase


```service sshd restart```

### Establishing connection
- 

### Run Python code
- TBC

[^1]: One of the Opentrons products


------ (updated August 1th)


1. To create the docker group and add your user:

2. Create the docker group: '''sudo groupadd docker'''

3. Add your user to the docker group: '''sudo usermod -aG docker $USER

4. '''newgrp docker '''

to check the architecture: '''dpkg --print-architecture''' (arm64)


 docker run -i -t imageID 
