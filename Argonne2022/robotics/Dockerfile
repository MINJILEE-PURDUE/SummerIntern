# Start from Waggle base image
FROM kwelbeck/base-ros2-with-empty-overlay:arm64

# Install linux packages
RUN apt update && apt install -y zip htop screen libgl1-mesa-glx

# Install python dependencies
COPY requirements.txt .
RUN python -m pip install --upgrade pip
RUN pip uninstall -y torch torchvision torchtext
RUN pip install --no-cache -r requirements.txt albumentations wandb gsutil notebook \
    torch==1.10.2+cu113 torchvision==0.11.3+cu113 -f https://download.pytorch.org/whl/cu113/torch_stable.html
# RUN pip install --no-cache -U torch torchvision

# Create working directory
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

# Copy contents
COPY . /usr/src/app

# Downloads to user config dir
ADD https://ultralytics.com/assets/Arial.ttf /root/.config/Ultralytics/
# Creating directory for decoded yamls
RUN mkdir -p /root/config/temp

# Downloading ot2_driver, installing dependencies and changing ownership from root
# Could alterntively change permissions instead
WORKDIR /root
RUN git clone -b dev-kyle https://github.com/kjwelbeck3/ot2_driver.git \
    && pip3 install -r ot2_driver/requirements.txt \
    && useradd user \
    && chown user:user ot2_driver \
    && mkdir -p /root/

# Downloading ros packages and Creating an overlay
RUN mkdir -p $ROS_WS/src
WORKDIR $ROS_WS/src
COPY ros-packages .
RUN vcs import < repos
WORKDIR $ROS_WS
SHELL ["/bin/bash", "-c"]
RUN source $ROS_ROOT/setup.bash && colcon build --symlink-install && source $ROS_WS/install/setup.bash

# On image run, source overlay and launch node
COPY ros_entrypoint.sh /
ENTRYPOINT [ "/ros_entrypoint.sh" ]
CMD ["ros2", "run", "demo", "action_server"]
