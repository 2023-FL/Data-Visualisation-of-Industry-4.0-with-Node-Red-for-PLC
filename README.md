# Data Visualisation of Industry 4.0 with Node-Red for Mitsubishi PLC

## Installation Manual of PLC connecting with sensors and other electric device

Step 1: To follow below diagram for connecting all electric wires between PLC, electric devices and sensors
Installation of Temperature Sensor connected with Temperature Module of Mitsubishi PLC
![image](https://user-images.githubusercontent.com/57984642/164303462-4cb2daa9-3c70-4485-8952-89be6da89138.png)

Step 2: To follow below diagram for connecting electric wires of temperature sensor with Mitsubishi Temperature module
![image](https://user-images.githubusercontent.com/57984642/164303515-0740f382-fbe3-4aaa-81ef-3171929ba8e1.png)
 
Step 3.1: Start MELSOFT GX Works application software, then go to tool bar and select “Engineering” (“工程”) as well as select “Open” (“打开”), 

![image](https://user-images.githubusercontent.com/57984642/164303552-570d76e7-d12e-4dd9-8261-9fd12a11aa27.png)
 
Step 3.2: choose Smart-Patch_Project_LED_Motion_sensor.gx3
![image](https://user-images.githubusercontent.com/57984642/164303572-281f9f3a-43e0-4adc-a34a-837228b05fa4.png)

Step 4: In the PLC program, go to toolbar and select “Monitor (write mode)”                                                           ![image](https://user-images.githubusercontent.com/57984642/164303593-b7af78ef-45e7-4e82-a90a-67df00f033e3.png)                                                                                                
Step 5: Start XAMPP database application by double clicking icon “ ” for launching Web Server of “Apache” and online SQL Database shown as below

![image](https://user-images.githubusercontent.com/57984642/164303641-477713c0-c2e8-4686-808f-54dd88a59839.png) 

Step 6.1: Open any Browser and then key in “Localhost:8080/phpmyadmin/” on domain name bar, you will see the following screen about PhPmyadmin panel

![image](https://user-images.githubusercontent.com/57984642/164303662-a5a99db3-3b2f-4817-b2f8-8ba7f62acd72.png)

Step 6.2: select “Browse” to see database records shown as follow
![image](https://user-images.githubusercontent.com/57984642/164303701-2f110475-64d2-4013-a826-cc72ee87fb78.png)

Step 7: Next, take your Smart-Patch device and switch it on by supplying it power, and then wait for Windows 10 OS being started up after 10 to 15 minutes; afterwards, typing “cmd” and select “Run as administrator” to open “Command Line Program”
![image](https://user-images.githubusercontent.com/57984642/164303722-fbf12821-22b7-44e3-8aef-662e27ab5c45.png)
  
Step 8: On the command line program, type “node-red” and wait for the message of node-red program to show “Loading palette nodes” after around 10 minutes.

![image](https://user-images.githubusercontent.com/57984642/164303754-6d100eef-abcf-48fd-aea3-7fb7a9e031a8.png) 

Step 9: Click on any browser and key in “localhost:1880” on domain name bar for launching Nod-Red Program
![image](https://user-images.githubusercontent.com/57984642/164303801-928d427e-d6e0-4729-8431-dd7b26c6f55f.png)

Step 9.1: After launching “IMPORT” function, go to bottom of the window and select “new flow”; then go to upper side of the window for clicking on “select a file to import”. 

![image](https://user-images.githubusercontent.com/57984642/164303842-dd89aaf3-e176-4c2f-8a7d-8cc5c23ec02b.png)
 
Step 9.2: Select files of (WashingMachine_Final_Version)Flows.json, (WashingMachine_final_Version)Flows2.json, Smart-Home(Final_Version)flows.json one by one to import them into the Node-red program

![image](https://user-images.githubusercontent.com/57984642/164303862-f89c9e6c-36b2-4450-9184-681c335bcf84.png)

Step 10: Go to upper-right-hand-side of the program and select symbol “ ” for choosing IMPORT function.
![image](https://user-images.githubusercontent.com/57984642/164303820-728a1d8d-ac36-4a71-b668-44d1be63361c.png)
  
Step 10.1: You will see the following those node-red flows (“流程”) of (WashingMachine_Final_Version)Flows.json, (WashingMachine_final_Version)Flows2.json, Smart-Home(Final_Version)flows.json one by one; then, select “流程2” , you will see Blue box in which there boxes are mentioning “WRITE_X0_1_FX5U_192.168.1.234:502, this mentions connection between node-red program and the PLC with IP address of Mitsubishi PLC. Just move the blue box forward by moving mouse to highlight the blue box and moving it forward, you will see right-hand upper corner of the symbol of “Deploy” that will be switched to Red colour. Just double click on “Deploy” for launching updating the connection bewteen Mitsubishi PLC and “流程2” of Node-red program. So do the same action on flow 2 for launching connection between Mitsubishi PLC and Smart-Home flow as well.
![image](https://user-images.githubusercontent.com/57984642/164303890-c6ebe22d-cf9b-4c1c-95a1-e2cef56cf931.png)
 
Step 10.2: You will see that there is green signal under each blue box to show “connected” for PLC and connected in term of “OK” for Database shown as follows

![image](https://user-images.githubusercontent.com/57984642/164303913-7b60bf96-9e29-4767-9f27-18c516e42af2.png)
 
Step 11.1: Washing Machine dashboard and Smart-Home dashboard can be shown by typing “localhost:1880/ui” on domain name bar of the browser; if want to see Smart-Home dashboard webpage, you can click on the upper left-hand side icon “                “ to show all ui webpages and then select of Home Floor Plan shown below second diagram.

![image](https://user-images.githubusercontent.com/57984642/164303933-0063b35b-5a10-46a0-898c-f302c10c64cc.png)
 
![image](https://user-images.githubusercontent.com/57984642/164303969-583aee2d-2b43-44de-8afe-e26e7581af99.png)
 
Step 11.2: After selecting the Node-red dashboard of HOME FLOOR PLAN shown as follows, you can see the blubs were turned on in term of yellow colour shown on the dashboard. When the blubs were turned off, the colour of those blubs are grey. The indoor temperature is as same as the temperature value shown on the dashboard of Washing Machine.
![image](https://user-images.githubusercontent.com/57984642/164303982-aa242ea3-c05c-40f7-b6db-d0ebfc0b18d3.png)
 
Step 12: Trouble Shooting. When you found out any problem of “connection lost” in between PLC, the simulation of monitor function of Mitsubishi GX Works software and Node-red dashboard software, you can turn off the Node-Red dashboard and start it again by following steps.
 Step 12.1: Click Command Line Window and press “Ctrl + C” button for stopping Nod-Red, then key in “Y”, then the Node-Red program will be turned off.
Step 12.2: Plug out the power from the PLC and then power on it again after 1 minute; go back step 8, key in “node-red” on command line window again for starting Node-red program and follow step 9 to step 11 again.
![image](https://user-images.githubusercontent.com/57984642/164304480-019154fa-1bc9-4b57-a4b0-ddc5dd700683.png)

(This fundamental tutorial about how to carry out data visualisation with Node-Red for PLC, it supposes that you have basic knowledge on installing Node.js, Node-Red and XMAPP database server firstly)

[![video](https://img.youtube.com/vi/188UED5zLjM/0.jpg)](https://www.youtube.com/embed/188UED5zLjM "Click to play on Youtube.com")
<iframe width="560" height="315" src="https://www.youtube.com/embed/188UED5zLjM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<div class="container">
<iframe class="responsive-iframe" src="https://www.youtube.com/embed/188UED5zLj"></iframe>
</div>
