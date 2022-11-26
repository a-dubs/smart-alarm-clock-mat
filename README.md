# Boilerplate for Projects on GitHub

My smart alarm clock that is turned off only by standing on a pressure sensitive mat created using a Raspberry Pi Zero W and my home server 

<br>

## Summary
 - This project had 3 different pieces
   - The smart mat  
     - Pressure sensitive mat that acts as button of sorts - when stepped on, its resistance drops to nearly zero and allows current to flow through.
     - Raspberry Pi Zero W that runs a python script which sends HTTP requests to the API hosted on my server
       - Sends periodic "heartbeat" POST request every 30 seconds
       - Sends POST request whenever the state of that mat changes
       - Has ghosting/accidental step off prevention - mat's state must change for >5 seconds before POST request gets send to API 
   - The alarm clock software and automation on my phone  
     - "Wake me up!" Android app provides the alarms that are monitored and triggered by "Tasker"  
     - "Tasker" Android app monitors and triggers alarms provided "Wake me up!"   
     - The Tasker app is where all of the logic lives:
         - Request current state of the mat (stood on / not stood on) every minute
         - If mat is not being stood on, retrigger the alarm and reset the minutes stood on counter  
         - If 10 consecutive iterations (each 1 minute long) occur where the mat is stood on, then disable the alarm
   - The public API hosted on my server 
     - Node.Js with Express 
     - Receives the mat's current state and filters out false positives

<br>

## Image Gallery

### Placeholder Image (This is the image's caption/label)
![Please end my suffering... (This is the image's alt text)](/image_gallery/Please%20replace%20me%20I%20am%20begging%20you.jpg)
<br>

<!-- 
### (This is the image's caption/label)
![(This is the image's alt text)](full_http_path_to_image)
<br> 
-->

<br>

## Project Metadata

**Project Status** : Active  
**Project Progress** : Completed  
**Project dates** : Dec '21 - March '22  

