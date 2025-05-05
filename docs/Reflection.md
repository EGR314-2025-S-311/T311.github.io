---
Title: Team Reflection
---
## Lesson Learned
There were several challenges that the team learned throughout the semester while working on the project but through these experiences, the team was able to persevere and learn from their mistakes. One major lesson that comes to mind includes referring to the datasheet, especially during hardware design as minor mistakes can cost you a lot of time and money. Some teammates faced several last minute decisions which caused the team to shift the project scope nearing the Innovation Showcase. We also should always check if components are compatible with each other, either being done through research or examining the datasheet. At times, the team came across issues where some components were not compatible with each other, especially the HMI subsystem or even the sensors. Getting more technical, another valuable lesson that the team learned was understanding how API works. It was a major roadblock during the semester that caught the entire team off guard. It's also important to tackle problems early on, especially during the debugging phase as many changes were made last minute due to how the team tackled problems. Another vital technical lesson the team learned during this phase was on understanding how crucial an oscilloscope was, especially during testing for serial communication (I2C and SPI). Without an oscilloscope, the team would have never been able to get his far throughout the project. 

Some lessons that revolve around the whole team during the project include communication. The team learned that communication was key throughout the semester as it allowed us to tackle project deadlines and set team goals throughout the semester. This included coming in early before class to test our daisy chain and sometimes even work together to solve problems other teammates were facing with their individual subsystems. This also directly correlates to time management and organization within the team. Rather than waiting till the last minute to complete assignments, the team created a cushion to ensure assignments were completed on time and to the best of our ability.  Another lesson the team learned together was embracing an iterative development process by breaking things down into smaller parts rather than tackling something all at once. The team worked together to first establish a successful API and message structure before taking on each individual subsystem so when it came time to test the daisy chain, it would be easier. 

At the end of the semester, a very important lesson that the team learned was being capable of adapting under pressure. Most of the team’s subsystems did not pass earlier stages of development, resulting in a loss of morale within the team. But through adapting and fast decision making, the team managed to have four working subsystems by the Innovation Showcase. It’s also important to just enjoy the little successes you get throughout the semester, a very valuable lesson the team learned throughout the semester. You should never expect projects to work the first time. Reflecting on how the team did, it reached a point where most of the team thought they were going to fail the project, but with last minute decision making, the team was successful in having a fully functional prototype.


## Recommendations for For Students

<ol>
  <li>
    Students need to build a strong foundation in time management and organization skills. This class was exceedingly harder than EGR 304 and required a lot more time to be allocated outside of class to be successful. Students can break tasks into smaller steps and also tackle problems early on so there is more time to seek help.
  </li>
  <li>
    Students should not be afraid to seek help from both professors and teaching assistants. They were in the same shoes at one point, so asking questions and going to office hours are crucial, especially when you are stuck.
  </li>
  <li>
    Students must understand the value of the datasheet and do research beforehand, especially during component selection. This is important as these problems can cause massive issues down the road, especially during PCB design or software development.
  </li>
  <li>
    Students should use components that are already applicable in labs such as a voltage regulator, stepper motor driver, or even some sensors. This is due to the fact that you already have it working on a breadboard if you were successful with the lab, making it very simple to create a working schematic with the SMD variant of the part.
  </li>
  <li>
    Students should have multiple options to fall back upon, especially when something does not work. This could include purchasing extra components or even different components if you later figure out some are not compatible with each other.
  </li>
</ol>



## Version 2.0
To improve communication amongst subsystems, the team would add messages that would check other systems. If one message gets sent to another board, both the sender and receiver will be notified. This removes the grey area of communication between the two boards. That way, each message will be noticed. Another improvement is properly implementing a broadcasting message ‘X’ in the system. That way, every single board can be shown to connect to one singular message in unity. Another feature to be added is more flexibility in message sending and receiving. To divide the work for future coding projects, the team would focus more on what types of messages are being sent and received first, rather than focusing on functionality. The team would work together to take the time to ensure that each message was being sent exactly the way it needed to be and that all boards could communicate before functions coded in, such as spinning motors or blinking LEDs. To improve debuggability, the team would implement new ways to display data visually. This means a screen on every device or an LED that confirms the sending and receiving of messages, rather than guessing. Finally, to make the code more stable, proper timers and delays would be perfected and implemented so that messages can be sent as cleanly and quickly as possible. 
