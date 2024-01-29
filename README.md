# Setup 
### Windows
1. Install docker desktop 
2. Pull the image using ```docker pull ros:foxy```
3. Install vcxsrv ```choco install vcxsrv``` (Run the terminal in admin mode)
    1. https://dev.to/darksmile92/run-gui-app-in-linux-docker-container-on-windows-host-4kde
    2. You may need to install choco first if you don't have that on your system 
4. Run XLaunch program and run through the default configuration (Disable Access Control) and save the configuration to %userprofile%\Desktop
5. Run ```docker run -it --net=host -e DISPLAY=[your-ip-address]:0.0 ros:foxy```
    1. For [your-ip-address], do ```ipconfig``` and find the ip of your local machine

Import notes: 
1. After going through all the ros foxy installation, don't forget to source the setup file. Ideally, input the 
```source /opt/ros/foxy/setup.bash ```
into the ~/.bashrc file
2. When you want to open up another terminal or want to continue on the same image you made with the `docker run -it ...`, use 
```docker exec -it [container-name] bash```. 

### Ubuntu
For ubuntu systems, installing ROS directly on the system is recommended

### MacOS
Follow the installation steps shown here in the github but change out the ros:latest with ros:foxy
https://gist.github.com/vfdev-5/b7685371071036cb739f23b3794b5b83
