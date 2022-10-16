# MyRobot : Training

**1. Create a training package**

-Go to the ros2 workspace : cd ros2_ws/src

-Create the learning package : ros2 pkg create --build-type ament_cmake learning (C++)

-Create the learning package : ros2 pkg create --build-type ament_python learning (Python)


**2. Publisher and subscriber**

Thanks to https://docs.ros.org/en/foxy/Tutorials/Beginner-Client-Libraries/Writing-A-Simple-Py-Publisher-And-Subscriber.html

Once your package is created, go to your package to learning/src in C++ or learning/learning in Python and type the 2 following commands :
wget https://raw.githubusercontent.com/ros2/examples/foxy/rclpy/topics/minimal_publisher/examples_rclpy_minimal_publisher/publisher_member_function.py
For an example of a publisher

wget https://raw.githubusercontent.com/ros2/examples/foxy/rclpy/topics/minimal_subscriber/examples_rclpy_minimal_subscriber/subscriber_member_function.py
For the subscriber

-Modify the entry point part of the setup.py file in the package :

**entry_points={
        'console_scripts': [
                'my_publisher = navigation.publisher_member_function:main',
                'my_subscriber = navigation.subscriber_member_function:main',
        ],
},**

Then in /ros2_ws :

**colcon build --packages-select learning**

Then :

**. install/setup.bash**

Open a terminal and type :

**ros2 run learning my_publisher**

Open an other terminal and type :

**. install/setup.bash**

And :

**ros2 run learning my_publisher**
