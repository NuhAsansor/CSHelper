#CSHelper
Script for AIESEC in Italy MKTG Tool's CS Page-Google Calendar Synchronisation

My name is Koru, the MKTG VP of AIESEC in Padova. This is a small script I wrote on Google's Apps Script for recording the booked Class Shouts of '💡CS funnel tracking' sheet of B2C/MKT Tracking Tool onto a Google Calendar dedicated to a team/Area. 

HOW TO USE: 
Open the sheet in the Spreadsheets you'd like to set the script in

Go to 'Extentions' -> 'App Script'

Log in and paste the code. 

Add a new service from top left and search 'Google Calendar API' that allows you to use the codes related to Google Calendar synchronisatiom

Make sure to update this line with the ID of the Google Calendar you'd like to connect your SpreadSheets to:
const CALENDAR_ID = "longStringOfNumbers@group.calendar.google.com"; // Replace with your Calendar ID

Ensure that the mail address you'll be using when accessing the Spreadsheets and Apps Script is authorised to edit your calendar, and is subscribed to it. Do all the necessary authorisations that the website will guide you through.

If you'll use your aiesec mail address you'll have to confirm that the script is safe, and inform your MCVP just in case.

Go to 'Triggers' and 'Add Trigger', then select event source as 'time-driven', and your time based trigger along with how often you'd like it to be updated. 

By changing the chosen columns within the code you can easily modify the data you'd like to save based on your column name and number.

Once all is set, manually execute it by clicking 'Run' for the first time to add all previous CS done to your calendar. Wait for the execution to end.

You can manually execute it whenever you want or set the trigger's time interval to 30 minutes so the script will modify the calendar for all edits done, and also check for duplicates.



OTHER THINGS TO NOTE:
It parses time by assuming that the grid containing it is of object type 'Date' (Opens small calendar interface when clicked), in format DD/MM HH:MM or DD.MM HH/MM

It also assumes that the end date for the event is 30 minutes after the start date. If there's no hour specified, the event is added to 00:00



