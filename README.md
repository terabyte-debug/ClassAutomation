# ClassAutomation

This bot gets the meeting ID of your meeting from Google Docs (note: your friend can upload this for you if you can't) and opens Google Meet and logs in on your behalf.

It can use both Speech Recognition and Image Processing techniques to interact with other people in the meeting.

Once the meeting is done, it closes the Google Chrome page and this process continues every time you have an online class to attend.

Speech Recognition is used to identify whether your enrollment number is being called out during attendance and the bot automatically types "present" in the chatbox.

Image Processing is used to convert all the messages in the chatbox into an array of strings and uses some string manipulation techniques to find the most common phrase most of the students said and type it in the chat box. For example, if 5 people said the answer was "11.5", the bot will type "11.5" in the chatbox and send it.

# Usage 

Step 1: First install all the requirements using pip
Note: This code supports only python3

Step 2: After installing all the requirements use the command python3 bunk_bot.py

### Changing the coordinates in PyAutoGUI is more than enough to implement this code on Google Meet, Zoom Meetings, Microsoft Teams or any other software you use to attend class.

CHANGES YOU HAVE TO MAKE:
A small amount of the code you see in this repository is hardcoded w.r.t to my computer. Changes that you have to make to implement this on your computer are:

Change all the coordinates that PyAutoGUI uses. Refer to coordinate_finder.py to find the coordinates which are suitable for you.
Change all the file paths.
Change the size of the crop in crop=img1[280:911,1520:1900] to crop=img1[y1:y2,x1:x2] where x1, x2, y1 and y2 are coordinates of the chatbox in the online classroom software (i.e Google Meet/ Zoom etc.)
These changes can be made in the global variables that is mentioned in the bunk_bot.py file. Can be found in the 15th line.
