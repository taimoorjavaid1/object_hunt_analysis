# Task: Data Analysis Report
The data provided contains information about a random selection of 5,000 players who installed one of our apps, Object Hunt (App store pages: Android and iOS), over a 30 day period.

There are two datasets provided:

players.csv:
Description: Event sent when player installed the app and contains information on the characteristics of the player.
Columns:
install_datetime: The date and time at which the player installed the app. (UTC)
player_id: A unique identifier for each player.
platform: The platform on which the player has installed the app.
country: The two digit country code representing the country of install.
screen_size: The diagonal screen size in inches. 
system_memory: The amount of RAM on the system in MB.

level_progress.csv:
Description: Event sent when player progresses through the levels and stages in the app.
Columns:
event_datetime: The date and time at which the event was received (UTC)
player_id: A unique identifier for each player.
level_number: The level number the event corresponds to. 
stage_number: The stage number the event corresponds to. A stage is a subsection of a level (i.e. a level will be split into a number of stages). For more information on level and stages see Appendix.
status: The outcome the event corresponds to:
‘start’: Sent when a player starts a stage within a level in a session. This can be re-sent for the same level if a player reboots the app and restarts the stage.
‘fail’: Sent when a player fails a stage within a level. In this app, a player fails when they are caught by the hunter. Failing results in the player receiving negative feedback text and will progress onto the following stage.
‘complete’: Sent when a player successfully completes a stage within a level and is eligible to progress onto the next level.
session_id: A unique identifier for the session in which the event was produced. A session is defined as the period of time a player plays the app, it starts when they open the app and ends when they close the app. A player can play for multiple levels and stages in a session.

You should use the player_id columns in each file to link players with their level progress information. 

Does failing a level increase the risk of churn? (Churn is the proportion of players who stop playing the game, i.e do not progress.)

Objective: Write a presentation which answers the question above
Assume that the customers will be game designers who will use this report to decide whether failing a level increases the risk of churn for this game.
You should start with simple analyses and techniques before exploring more advanced ones.
Your short report should take the following format:
Key results (1 slide): Brief summary on the main takeaways and conclusions.
Introduction (1 slide): Outline the aims and objectives of the analysis.
Methodology (1 slide): Describe any definitions, techniques and statistical methods used.
Results (max 3 slides): Display key findings using clear data visualisations, tables and bullet points.
Further analysis (1 slide): Describe any further analysis you would like to perform with this or similar data.
Any code you have written to produce results should be submitted separately.
