#Weekly Wrapped // Your Listening Analytics

##Purpose:
In response to Spotify's "Wrapped" and its subsequent success and impact on engagement, we developed Spotiflow, a feature within the Spotify application aimed at allowing users to visualize their recent listening trends—dubbed their 'vibe'—and share these insights with friends.

##Audience:
The SpotiFlow weekly wrapped user dashboard was created to enhance the Spotify user experience by providing more personalized and frequent insights into users’ listening habits.

###How does the dashboard address the business problem?
The dashboard allows users to interact with their previous listening data on a much more relevant, recent, and granular level. Because of this, we expect that weekly wrapped will boost engagement. 

###Identify the business process that utilizes the dashboard for decision making.
User recent listening data retrieved from Spotify API using Python.

Which decisions are influenced by the dashboard?


##Access:
https://public.tableau.com/app/profile/diego.estuar/viz/SpotiFlowUserDashboard/SpotiFlowWeeklyWrapped

##Data Source(s):
User recent listening data retrieved from Spotify API using Python.

##Key Metrics:
Energy Score
Musicality Score
Listening Vibe
Weekly Listening (# of Songs)
Weekly Top Songs
Total minutes listened

###Define the metrics and explain any calculations
Energy Score
  - Weighted average of danceability, energy, and liveliness feature data
Musicality Score
  - Weighted average of acousticness and instrumentalness feature  data
Listening Vibe
  - If the average valence feature data is:
        < 25%, "Is Everything Okay?"
        25% - 50%, "Slightly Sad"
        50% - 75%, "Feeling Great"
        > 75%, "A Little Too Happy"
Weekly Listening (# of Songs)
  - Count of songs by date
Weekly Top Songs
  - Count of total songs listened for dater ange
Total minutes listened
  - Sum of minutes listened
    
##How to Use the Dashboard
The dashboard is publically available and has several "drill down" features.
1. Select date to drill down and view listening a analytics for that day
2. Drag the "Top Songs" slider to adjust the number of top songs that are viewable

##How to Refresh the Data
Data must be refreshed manually.
1. Fetch data from Spotify API
2. Python to AWS
3. AWS to Tableau Prep
4. Tableau Dashboard
