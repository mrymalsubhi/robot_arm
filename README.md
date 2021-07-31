# robot_arm
## First task.


- الخطوة الاولى: نقوم بتثبيت نظام الروز ميلودك

```sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'

sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654

sudo apt-get update

sudo apt-get install ros-kinetic-desktop-full

apt-cache search ros-kinetic

echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc
source ~/.bashrc

sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential

sudo apt install python-rosdep

sudo rosdep init

rosdep update
```



---

- الخطوة الثانية: نقوم بتثبيت الcatkin واللذي نستطيع من خلاله عمل الwork space  

`sudo apt-get install ros-noetic-catkin`

---

- الخطوة الثالثة: نقوم بانشاء الwork space من خلال الاوامر:


```mkdir -p ~/catkin_ws/src

cd ~/catkin_ws/

catkin_make```

---

- الخطوة الرابعة: نذهب الى المجلد source
 
`cd ~/catkin_ws/src`

---

- ومن مجلد "source" نقوم بالدخول الى الباكجز الخاصة بالمسارات الذكية

`git clone https://github.com/smart-methods/arduino_robot_arm.git`

---

- الخطوة الخامسة: نقوم بالعودة الى مجلد catkin لتثبيت بعض الاوامرالخاصة بالروز 

`cd ~/catkin_ws`

---

- الخطوة السادسة: نقوم بكتابة الاوامر 

```sudo apt-get install ros-kinetic-moveit

sudo apt-get install ros-kinetic-joint-state-publisher ros-kinetic-joint-state-publisher-gui

sudo apt-get install ros-kinetic-gazebo-ros-control joint-state-publisher

sudo apt-get install ros-kinetic-ros-controllers ros-kinetic-ros-control```

---

- بعد اضافة جميع الاوامر نذهب الى الملف 

`sudo nano ~/.bashrc`

---

- ونضيف في النهاية الامر 

`source /home/maryam/catkin_ws/devel/setup.bash`

---

- ومن ثم
ctrl + o

inter ومن ثم

ctrl+x ومن ثم 

---

- source نقوم بتحديث ملف  
`source ~/.bashrc `

---

- الخطوة الاخيرة: نقوم بتشغيل برنامج المحاكي من خلال الامر  
`roslaunch robot_arm_pkg check_motors.launch`

---

![7aecfc61-ee15-459b-9345-e8c27dfe4927](https://user-images.githubusercontent.com/85639068/127725522-1a9f9c17-3f25-4eb2-8b54-b87d51203f5c.JPG)


---

- ومن ثم نستطيع التحكم بالذراع

---

![028c269a-0f47-4c6d-9318-5464d68b72a3](https://user-images.githubusercontent.com/85639068/127725527-212150e3-8d72-436f-a830-d96c9f783b27.JPG)







