# Controlling-the-robot-arm-by-joint_state_publisher



### step1: Create a ROS Workspace (Catkin)

```mkdir catkin_ws```
then you can go inside your new folder:

```cd catkin_ws ```
then we are going to create a source (make sure it it exactly src inside thr catkin work space)

```mkdir src```

![image](https://github.com/user-attachments/assets/aab89254-1c5e-42bb-8864-a55d6fb27e9f)


now make sure that you are inside the catkin_ws folder (not inside the src folder) then we can start to compile by running the command :

catkin_make


![image](https://github.com/user-attachments/assets/8a619c9a-a412-4161-972f-f18f962a3168)


basicaally this is gonna compile everything in the workspace, install stuff, etc...

now if we run the command ls we see that we have two new folders (build and devel)

if you go to the devel folder : cd devel/ then ls


![image](https://github.com/user-attachments/assets/065e97a9-87dc-458a-8e29-13764cebf5aa)








here we see something called (setup.bash) we will need to source this (setup.bash) script if we want to be able to use the code that we have written in our catkin workspace.

so, to source this we will need to:

```source ~/catkin_ws/devel/setup.bash```

once you have run this command you can use your custom ROS code

last thing here is to run``` gedit ~/.bashrc``` then this window will appears


![image](https://github.com/user-attachments/assets/61755258-e034-49d9-96e0-b74387e2f2d6)



at the end or the window we have the source line for our global ROS installation . so we will add this line source ~/catkin_ws/devel/setup.bash (after) the global ROS installation


![image](https://github.com/user-attachments/assets/594daabf-6f7d-4da9-9fc2-33ce9e69ac6e)









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

![image](https://github.com/user-attachments/assets/38e24a66-d383-4ba9-994e-56cf01665f54)


### Gazebo


run the command :

```  roslaunch robot_arm_pkg check_motors_gazebo.launch  ```


![image](https://github.com/user-attachments/assets/e56b5881-89df-40c4-b7ac-303d1e34d1e0)



### MoveIt controlling

```  roslaunch moveit_pkg demo.launch  ```

![image](https://github.com/user-attachments/assets/09e97638-fd7b-4426-8577-6b8c163bcb63)









