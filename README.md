# wro2023-fe-Zhabailar
Engineering materials for a self-driving machine serves as a robotic solution for the Republican phase of WRO

![image](https://github.com/adst0rm/wro2023-fe-Zhabailar/assets/113520087/9911cddb-9371-4ffa-8965-75ed7f5c3c3d)


### About repository
This repository contains all important files and information about our autonomous-driving car "Zhabailar". As a base/microcontroller, we chose the Lego Mindstorms EV3, which we equipped with the PixyCam CMUcam5 V2 (Lego Mindstorms version) for object recognition. The reasons for choosing the EV3 were the high reliability as well as the already existing knowledge and experience with the system from Lego incl. programming. We developed the program for the regional competition, which took place for us in Uralsk, in the Lego software based on LabView. All "V1" files are relevant for the Uralsk regional phase. The software ran on an EV3 brick with the original Lego Mindstorms EV3 firmware. For the Kazakhstan final phase of WRO, we went a step further and tried to program the EV3 brick based on the ev3dev firmware using Python. Hope was increased flexibility and versatility. For the world final in Kazakhstan, we modified the robot a bit to reach higher speeds. Going faster also meant some changes in the software. All "V2" files are relevant for the Kazakhstan final cup.

### Program structure
The programs changed a lot over rounds of competition. As mentioned earlier, we used Lego software based on LabView in the beginning. For the Uralsk Regional Phase, the goal was to complete the races with Python programs. We did not succeed in this, which meant that during the competition we reverted to .ev3, which was already working. For the Kazakhstan finals, we relied on improved Python programs. Since we use different sensors for the two race modes, we created a script for the race without obstacles (for Kazakhstan finals see "/Programmcode/Python/non-obstacles.py") as well as a script for the obstacle race (for Kazakhstan finals see "/Programmcode/Python/obstacles.py"). We also wrote a module ("/Programmcode/Python/felib.py") which contains important functions for "obstacles" and "non-obstacles". An example is the myPID class, which provides a PID controller and calculates motor values from setpoints and actual values.

### Motors/sensors
The robot was driven by a Lego EV3 medium motor via the rear axle with differential (better cornering). For steering, we also used a Lego EV3 Medium motor connected to a steering device. To make the bot drive as straight as possible, we initially installed a Lego gyro sensor, which was reset after the start and then measured the turning position. Furthermore, a Lego color sensor detects if a colored line is crossed. This is useful for counting sections and stopping after three laps on the one hand, and initiating a turn on the other. Before an obstacle race, we mount the aforementioned PixyCam to drive around the red and green obstacles. We were not able to distinguish the thick and colored lines from the obstacles with the camera and to evaluate them in a meaningful way to do without a color sensor. During a race without obstacles, the robot also orientates itself with the help of two Lego ultrasonic sensors, which measure the distances to the walls. One of the measures to the left side and the other to the front side. For a higher speed, we installed a Lego EV3 Large motor with transmission before the Kazakhstan final. But in the curves, we had to slow down the speed to recognize the colored lines because we had trouble with it.

### Software
We programmed the .ev3 in Lego's own LabView environment and the .py in Microsoft Visual Studio Code with the ev3dev extension. The 3D model, engineering drawing, and electrical component representation were created in Autodesk Fusion 360..

### About Us
**About Us: Mukanov Daulet and Ergen Adil - Pioneers in Engineering and Robotics**

Embark on a journey through innovation and technology with us, Mukanov Daulet and Ergen Adil from Uralsk, as we unravel the story of our lifelong friendship and our shared passion for engineering and robotics. Our tale is one of curiosity, determination, and the relentless pursuit of turning dreams into reality.

**Kindred Spirits in Curiosity**

Our story begins years ago in the vibrant neighborhoods of our childhood. From a young age, we both displayed an insatiable curiosity about how things worked, often spending hours dismantling and reassembling gadgets just to understand their intricate mechanisms. Our parents fondly remember our early fascination with machines, a foreshadowing of the remarkable journey that awaited us.

**A Meeting of Minds**

Fate brought us together, aligning our paths in the hallowed halls of a prestigious engineering institution. It was here that we realized our shared dreams and embarked on a journey that would forever change the trajectory of our lives. Our minds found common ground as we delved into the world of robotics, fueled by the desire to push the boundaries of what machines could achieve.

**Boundless Dreams, Relentless Pursuit**

Our collaboration quickly transformed from late-night discussions to ambitious projects that challenged the conventional norms of robotics. The challenges were immense, but so was our determination. Together, we navigated the intricacies of programming, mechanics, and artificial intelligence, learning valuable lessons from every setback and celebrating each triumph as a testament to our teamwork.

**From Blueprint to Reality**

The culmination of our efforts came to life in the form of our groundbreaking robot. Countless hours of design, programming, and experimentation gave birth to a marvel of technology that surpassed even our wildest imaginations. Our creation not only showcased our technical prowess but also reflected the deep bond of friendship that fueled our journey.

**A Glimpse into the Future**

As we stand on the precipice of a new era in robotics and automation, our passion burns brighter than ever. Our story is a testament to the power of friendship, curiosity, and the relentless pursuit of knowledge. Together, we look ahead to a future where our innovations continue to shape the world of engineering and robotics, inspiring generations to come.

Join us as we continue to explore the uncharted territories of innovation, pushing the boundaries of possibility, and redefining the relationship between humans and machines. The adventure is far from over, and we invite you to be a part of our journey into the ever-evolving realm of engineering and robotics.

Mukanov Daulet and Ergen Adil
*Pioneers, Innovators, Friends*
