# robot_arm
## First task.


- الخطوة الاولى: نقوم بتثبيت نظام الروز ميلودك

`sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'

sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654

sudo apt-get update

sudo apt-get install ros-kinetic-desktop-full

apt-cache search ros-kinetic

echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc
source ~/.bashrc

sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential

sudo apt install python-rosdep

sudo rosdep init

rosdep update`

---

- الخطوة الثانية: نقوم بتثبيت الcatkin واللذي نستطيع من خلاله عمل الwork space  

`sudo apt-get install ros-noetic-catkin`

---

- الخطوة الثالثة: نقوم بانشاء الwork space من خلال الاوامر:

`mkdir -p ~/catkin_ws/src

cd ~/catkin_ws/

catkin_make`

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
`rosdep install --from-paths src --ignore-src -r -y

sudo apt-get install ros-melodic-moveit

sudo apt-get install ros-melodic-joint-state-publisher ros-melodic-joint-state-publisher-gui

sudo apt-get install ros-melodic-gazebo-ros-control joint-state-publisher

sudo apt-get install ros-melodic-ros-controllers ros-melodic-ros-control`

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

![7aecfc61-ee15-459b-9345-e8c27dfe4927](https://user-images.githubusercontent.com/85639068/127724114-b8ccf9f0-5055-4fef-a072-b2b9617e19bc.JPG)

---

- ومن ثم نستطيع التحكم بالذراع

---

![2625be62-155f-44e8-bbc7-31b52b1b4f18](https://user-images.githubusercontent.com/85639068/127724157-f5294589-4299-4800-b6c2-e82ef7c1a73d.JPG)






