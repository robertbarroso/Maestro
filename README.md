# Maestro
Pomodoro-style studying application with Spotify integration that plays classical music as the timer goes down.

## Requirements
The requirements for this application is so that the user can utilize this clean and minimal Pomodoro-style application to increase their productivity by only working in short-bursts with an even smaller cool-down period. The application should ideally work with a single click of a button, where by default the timer is set to 20:00 minutes. When the user clicks "begin", the timer will begin to tick down until the timer reaches 00:00. From there, a bell will ring and the user is prompted to begin their short break of 05:00 minutes. The user may choose at the start a 20/5 minute configuration or a shorter 15/3 or a longer 60/10. The user also has the ability to enter in a "check list" where they get to check off what they have completed. Originally, I was going to make it where you can "queue" tasks that will automatically transition betwen workng and taking a break, but I found it not to be so accurate. What if a task takes a little too long, and now your entire studying/working queue is off? Might as well just have a check-list and you check off what you complete when you complete it. The user should also have the ability to skip either the working mode or break mode. 

The main feature that is different in this case is that there will be Spotify music component to this application. When connected (and the user *must* have Spotify Premium), then while the timer is going down, classical music shall play from various playlists on Spotify. Ideally one where the playlist is dynamic and changes so there's always something new. When the break time occurs, the music shall stop, and when the break is over, then the music shall return.

**Final Requirements**

*User perspective*
- User presses "begin" button, and the timer begins counting down - starting point is in "working" mode.
- User presses "begin" again when the timer expires to begin the "break" mode.
- User presses the "skip" button to skip modes (working/break).
- User presses the begin button to start the timer, and then the same button with "pause" on it to stop the timer. 
- User connects and signs into Spotify.
- User presses "begin" with Spotify connected, and classical music plays from the client.
- Users access controls to skip songs through Spotify
- User enters tasks in a check-list and can check off and delete entries into this check-list.
- User can check off tasks and that task will be added to a "completed" section

## Design
The program will consist of three main components: the timer section (the most prominent), the Spotify connection section, the check-list and the completed list. 

### The Timer Section
The most important part, this section contains the timer itself, that defaults to the 20/5 setting from before. There will be three buttons for controlling the duration: 15/3, 20/5, and 60/10. There will also be two additional buttons that begin the timer (which then turns to a pause button) and a skip button. 

### The Spotify Controls Section
By default, not connected. Will be greyed out until the user prompts to sign in. When signed in, the player will play from the browser a classical music playlist. Controls to play/pause, skip, and volume controls will be present. (Maybe a link to the playlist/song itself). 

### Check-list Section
User can add "tasks" to this list. A button to add is present to add an entry, a delete to remove an entry, and an edit to change the entry. To the left of the entry, is a check mark. 
When the user checks an entry, gets added to the completion section - grayed out and stikle line through below the current task.

                                                   

     |-------------------------------------|                |---------------------------|
     |                                     |                |                           |
     |                                     |                |                           |
     |                                     |                |        Check-list         |
     |                                     |                |                           |
     |           Timer Section             |                |                           |
     |                                     |                |---------------------------|
     |                                     | 
     |                                     |                |---------------------------|
     |                                     |                |                           |
     |                                     |                |      Spotify Connect      |
     |                                     |                |                           |
     |-------------------------------------|                |---------------------------|

