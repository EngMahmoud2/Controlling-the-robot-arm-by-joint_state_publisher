# Controlling-the-robot-arm-by-joint_state_publisher









### Installing the package arduino_robot_arm


1-  Add the “arduino_robot_arm” package to “src” folder cd src then copy this command :

```   sudo apt install git    ```

![image](https://github.com/user-attachments/assets/26b4f6b6-0d21-4512-9077-e7189a68abef)



2-  ``` git clone https://github.com/smart-methods/arduino_robot_arm   ```


![image](https://github.com/user-attachments/assets/8187d130-9bd4-4ae2-ad21-e87c29f69db9)




3-     now go back to the (catkin_ws) using command  cd .. ,then

```  rosdep install --from-paths src --ignore-src -r -y    ```

4- run the command

``` sudo apt-get install ros-noetic-moveit ```
![image](https://github.com/user-attachments/assets/dd5a08c3-168f-4106-942e-bef84a0c359a)



5 run

``` sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui ```

![image](https://github.com/user-attachments/assets/2d54ff23-14ec-4d8f-9d9d-498ce6729a36)


6-  run

``` sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher  ```

![image](https://github.com/user-attachments/assets/01ca94dc-cbbb-4eca-827e-dbeecdebaa18)




7- run

``` sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control  ```

![image](https://github.com/user-attachments/assets/51c2f861-c466-4680-b956-c2b3049fadfe)



8- compile the package

``` catkin_make ```

### Controlling the motors

when you run this command the widows will apears

```  roslaunch robot_arm_pkg check_motors.launch  ```

![image](https://github.com/user-attachments/assets/3ec2247b-21a9-4b5e-b56b-695279bc12ad)









