# Weekly Wrapped // Your Listening Analytics

## Purpose:
In response to Spotify's "Wrapped" and its subsequent success and impact on engagement, we developed Spotiflow, a feature within the Spotify application aimed at allowing users to visualize their recent listening trends—dubbed their 'vibe'—and share these insights with friends.

## Audience:
The SpotiFlow weekly wrapped user dashboard was created to enhance the Spotify user experience by providing more personalized and frequent insights into users’ listening habits. By providing users with personalized analytics on a weekly basis, it caters to an audience that values understanding their music consumption patterns. This frequent, personalized insight helps users to see how their tastes evolve over time and encourages deeper interaction with the Spotify platform. The dashboard is designed for users who enjoy reflecting on their music choices, discovering trends in their listening habits, and sharing these insights with friends, thereby making the Spotify experience more engaging and communal.

### How does the dashboard address the business problem?
The introduction of SpotiFlow's weekly wrapped dashboard is a strategic move to enhance user engagement with the Spotify platform. By allowing users to interact with their recent listening data at a detailed level, the dashboard makes the experience more relevant and personalized. This relevance is expected to increase user interaction with the platform, as users are likely to spend more time exploring their listening habits and discovering new music through personalized recommendations. The dashboard not only keeps users engaged but also encourages them to return to the platform regularly to check their latest insights, thereby increasing the frequency of engagement.

### Identify the business process that utilizes the dashboard for decision making.
The dashboard plays a critical role in the business process of enhancing customer engagement. By providing weekly insights into listening habits, it keeps the platform dynamic and interactive. This ongoing engagement feeds into Spotify’s larger strategy of retaining users and increasing the time they spend on the platform. From a business perspective, the dashboard serves as a tool for collecting data on user preferences, which can then be analyzed to fine-tune recommendation algorithms, improving the overall user experience and satisfaction.

### Which decisions are influenced by the dashboard?
The SpotiFlow dashboard influences both user and business decisions. On the user side, insights from the dashboard can lead to decisions about exploring new genres, artists, or playlists based on their weekly listening vibes and top songs. This self-reflection on music preferences can enrich the user's listening experience and encourage the exploration of Spotify's vast library.

On the business side, SpotiFlow leverages the data gathered from user interactions with the dashboard to make decisions regarding predictive recommendations. By understanding patterns in listening habits, Spotify can tailor its music recommendations more accurately, thus enhancing the personalization of the user experience. This data-driven approach to recommendations supports Spotify's objective of being the most personalized music service, ensuring that users continually discover music that resonates with their tastes and moods.

## Access:
https://public.tableau.com/app/profile/diego.estuar/viz/SpotiFlowUserDashboard/SpotiFlowWeeklyWrapped

## Data Source(s):
User recent listening data retrieved from Spotify API using Python.

## Key Metrics:
Energy Score
Musicality Score
Listening Vibe
Weekly Listening (# of Songs)
Weekly Top Songs
Total minutes listened

## Define the metrics and explain any calculations.
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
  - Count of total songs listened for date range
    
Total minutes listened
  - Sum of minutes listened
    
## How to Use the Dashboard:
The dashboard is publically available and has several "drill down" features.
1. Select date to drill down and view listening a analytics for that day.
2. Drag the "Top Songs" slider to adjust the number of top songs that are viewable.

## How to Refresh the Data:
Data must be refreshed manually.
1. Fetch data from Spotify API
2. Python to AWS
3. AWS to Tableau Prep
4. Tableau Dashboard
