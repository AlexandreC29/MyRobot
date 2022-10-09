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
