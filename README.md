# MyRobot : basic configurations


**1. Project creation**

On https://app.theconstructsim.com/MyRosjects : "Create a New Rosject"

Configuration :
- Type : Ros2 galactic
- Name : MyRobot : Smartbot
- Description : NULL


**2. Package creation**
- Go to the ros2 workspace : cd ros2_ws/src
- Create the navigation workspace : ros2 pkg create --build-type ament_cmake --node-name my_node navigation (C++)
- Create the navigation workspace : ros2 pkg create --build-type ament_python --node-name my_node navigation (Python)

**3. Nano installation**
- sudo apt update
- sudo apt install nano

# MyRobot : Training

**1. Publisher and subscriber**

Thanks to https://docs.ros.org/en/foxy/Tutorials/Beginner-Client-Libraries/Writing-A-Simple-Py-Publisher-And-Subscriber.html

Once your package is created through the PowerShell go to your package to the repository "src" in C++ or "navigation" in Python and type  the 2 following command :
- wget https://raw.githubusercontent.com/ros2/examples/foxy/rclpy/topics/minimal_publisher/examples_rclpy_minimal_publisher/publisher_member_function.py
For an example of a publisher
- wget https://raw.githubusercontent.com/ros2/examples/foxy/rclpy/topics/minimal_subscriber/examples_rclpy_minimal_subscriber/subscriber_member_function.py
For the subscriber and modify the entry point part of the setup.py file in the package : 
entry_points={
        'console_scripts': [
                'my_publisher = navigation.publisher_member_function:main',
                'my_subscriber = navigation.subscriber_member_function:main',
        ],
},

Then in /ros2_ws, type : 
