-------- INTRODUCTION --------

The 'ESP32_cam_google_drive.ino' file folder will allow you to run a program on your ESP32-CAM that will connect your ESP32-CAM to the internet, connect to google, periodically take photos and send them to a google drive folder. 'The ESP32_cam_google_drive_and_servo_motor.ino' file folder does the same thing, except it also rotates a servo motor between taking photos. 

The 'ESP32_CAM_GS.txt' file is a google script that will allow the ESP32-CAM to save photos directly to your google drive. 


-------- SET UP --------

Before running the .ino files, you must create the google script. To do this, do the following. 

1. Go to https://script.google.com/home/

2. Click 'New Project'

3. Paste the contents of 'ESP32_CAM_GS.txt' into the code space. Edit the time zone to yours and change the value of the folderName constant to the name of the folder in google derive that you would like to save your photos to. 

4. Click 'Deploy,' then click 'New Deployment.'

5. Select type 'Web App,' then change Who has access to 'Anyone.'

6. Click Deploy and authorize with your google id when prompted. 

7. Copy the deployment ID. This will be used in the .ino scripts


-------- RUNNING THE INO FILES --------

Save the the 'ESP32_cam_google_drive_and_servo_motor.ino' and 'ESP32_cam_google_drive.ino' file folders to your local device and open them using your IDE. In the .ino files, find the following lines of code:

const char* ssid = "****";
const char* password = "****";

ssid shold be set to your networks ssid and password should be set to your network's password. 

Below that, there will be the following lines of code:

String myDeploymentID = "Deployment ID";
String myMainFolderName = "Folder Name";

Paste your google script's deployment ID and the corresponding folder name.

Upload the two projects to two different ESP32-CAMs


-------- CONNECTINGE THE SERVO --------

The ESP32-CAM that the 'ESP32_cam_google_drive_and_servo_motor.ino' file was uploaded to should be connected to a micro servo motor. Connect the servo's positive wire to the ESP32-CAM's 3.3V pin, connect the servo's ground wire to the ESP32-CAM's ground pin, and connect the servo's signal pin to GPIO pin 13. 

-------- RUNNING THE CODE --------

The code will run automatically when connected to power and start taking photos and sending them to google drive.











