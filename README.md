# IOT_Obstacle-Avoidance-Vehicle
Ultrasonic Sensor Obstacle Avoidance Vehicle

A small autonomous vehicle I designed, built, and coded to navigate a known obstacle course using ultrasonic sensors and servos.

Tech used: Hardware(Arduino, Ultrasonic Sensors, servos) Software(C++)

Problem: To safely navigate an item to certain areas and return the vehicle safely without contact with "red zones" and to follow marked lines accordingly.

Solution: I used code to navigate the vehicle based on time per inch for most of the challenges dealing only with the servos, maneuvering forwards, backwards, arcing, and in a 180 single point turn. The line follow challenge was based of light, if the light was bright, turning back into the dark, and if dark, turning back into the white. This allowed me to maneuver the car safely to the destination. 

Challenges: The challenge was using crude and inefficient equipment (small servos) to do a precision task. These challenged me to understand voltage usage and understanding hardware out a higher level.

Improvements: I've since looked at my Rumba vacuum differently and how it tracks a sensor to maneuver through a home, park, and find "home." I have been thinking that i would add an output sensor and an input sensor to track locations and maneuver more easily around objects.
