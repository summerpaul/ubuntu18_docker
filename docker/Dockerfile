FROM tiryoh/ros-desktop-vnc:melodic

# ------ powered by paul xia, summerpaul917@qq.com ------

LABEL maintainer="summerpaul917@qq.com, Yunkai Xia"
RUN apt-get update -q --fix-missing && \
    apt-get install -y --no-install-recommends --allow-unauthenticated \
    ros-melodic-navigation \
    ros-melodic-libg2o \
    ros-melodic-mbf-costmap-core \
    ros-melodic-mbf-msgs \
    ros-melodic-costmap-converter \ 
    libgoogle-glog-dev \
    libgflags-dev \
    libnlopt-dev \
    libboost-all-dev \
	libboost-python-dev \
	libeigen3-dev \
	libgeographic-dev \
	libglfw3-dev \
	libglm-dev \
	libgtest-dev \
	libpugixml-dev \
	python3-catkin-tools \
	libpcap-dev \
	ros-melodic-angles \
	ros-melodic-camera-info-manager \
	ros-melodic-ddynamic-reconfigure \
	ros-melodic-diagnostic-updater \
	ros-melodic-geodesy \
	ros-melodic-jsk-recognition-msgs ros-melodic-visualization-msgs \
	ros-melodic-lanelet2 \
	ros-melodic-nav-msgs \
	ros-melodic-nmea-msgs \
	ros-melodic-tf2-sensor-msgs\
	ros-melodic-navigation*\
	ros-melodic-pointcloud-to-laserscan\
	ros-melodic-map-server

RUN apt install libjsoncpp-dev  -y

RUN git clone https://github.com/gabime/spdlog.git 
RUN cd spdlog && \
    mkdir build && cd build && \
    cmake .. && \
    make -j8 && \
    make install && \
    ldconfig
RUN cd .. && rm -rf spdlog

RUN git clone https://github.com/stevengj/nlopt.git 
RUN cd nlopt && \
    mkdir build && cd build && \
    cmake .. && \
    make -j8 && \
    make install && \
    ldconfig
RUN cd .. && rm -rf nlopt
