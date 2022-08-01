# Environment description to control/manage Opentrons under the Docker container
Prerequisites: Basic Linux experience, familiarity with single-board computers like a Raspberry Pi, and a basic skill of Docker/ROS.

### Table of contents:
1. Hardware needed
2. Enabling root SSH access
3. Establishing connection
4. Run Python code

### Hardware needed
- OT-2[^1] Robot and Pipette (version xx.1)
- Nvidia Jetson Nano installed and attachec JetPack 4.1.1 SD card image

### Enabling root SSH access
In order to enable the SSH access, run ```v```
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
