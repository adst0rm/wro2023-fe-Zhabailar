**In `/Program_Code/obstacles.py` we show our code to solve this trouble. Now we going to discuss this code and explain our strategy.**
**Pixy camera v2:**
![image](https://github.com/adst0rm/wro2023-fe-Zhabailar/assets/113520087/f0c3595f-d17b-4690-baa9-3afea730232b)


The provided code appears to be a Python script designed to control a robot's navigation and obstacle negotiation behavior using various sensors and actuators. Here's a breakdown of the code and the strategy it employs:

1. **Importing Libraries:**
   The script starts by importing necessary libraries, including math functions, EV3Dev2 motor and sensor classes, as well as custom functions from the `felib` module. It also imports the `LegoPort`, `Button`, and `threading` modules.

2. **Object Class:**
   The code defines an `Object` class that represents an object detected by the robot. This class has attributes such as color and sign, which seem to be related to the detected object's properties.

3. **Object Action Method:**
   The `object_action` method within the `Object` class is responsible for taking actions based on the detected object's position and height. It uses PID control to adjust the robot's steering to navigate around the detected object. The method includes different logic branches for different cases, such as passing, moving back, and aiming towards the object.

4. **Main Code Execution:**
   - The main part of the code is encapsulated in an `if __name__ == "__main__":` block, which ensures that the following code is only executed when the script is run directly, not when imported as a module.

   - The script initializes various motors, sensors (ultrasonic, gyro, color, and a camera), and variables for controlling the robot's behavior.

   - The robot's behavior can be broken down into three main sections:
     - **Initialization:** The robot calibrates its steering motor, resets the gyro sensor, starts a thread for tracking rotations, and waits for a button press to start.
     - **Navigation and Obstacle Avoidance Loop:** In this loop, the robot continuously drives forward while monitoring objects detected by a Pixy camera. It processes object data, calculating steering adjustments to either navigate around detected obstacles or follow an object.
     - **Completion and Cleanup:** Once a certain number of rotations are reached, the robot stops the drive motor and sets the steering to zero.

**Strategy for Obstacle Negotiation:**
- The robot primarily relies on a Pixy camera for detecting and categorizing objects. The objects are categorized based on their signature values.
- The robot uses PID control to adjust its steering and navigate around detected objects.
- The robot also interacts with ultrasonic and gyro sensors to assess the environment and adjust its behavior accordingly.

Please note that without a deeper understanding of the `felib` module's functions and the robot's physical setup, it's challenging to provide a comprehensive analysis. The strategy seems to be centered around using sensors and actuators to navigate around obstacles while following objects of interest.
