# SpotiFlow Diagnostic Dashboard

## Purpose:
Designed as an internal tool for Spotify, the SpotiFlow Diagnostic Dashboard offers comprehensive analytics on user listening behavior and model prediction accuracy. Unlike "Wrapped," which is consumer-facing, this dashboard provides Spotify with in-depth insights, fostering data-driven decision-making to refine user experience and model performance.

## Audience:
This dashboard is for Spotify's analytics and product teams. It equips them with detailed listening data and the precision of predictive modeling, enabling targeted improvements and personalized user experiences.

### How does the dashboard address the business problem?
The dashboard aids in identifying engagement trends and evaluating model predictions, crucial for iterating on Spotify's recommendation engine. Enhanced prediction accuracy can elevate user satisfaction and retention, directly impacting Spotify's market position.

### Identify the business process that utilizes the dashboard for decision making.
The SpotiFlow Diagnostic Dashboard feeds into the business process of continuous improvement and product development within Spotify. This process encompasses several key steps: monitoring real-time analytics for immediate insight, assessing the accuracy and efficacy of predictive algorithms, and integrating user feedback into the product life cycle. 

### Which decisions are influenced by the dashboard?
The internal-facing SpotiFlow Diagnostic Dashboard is designed to influence key business decisions that drive strategic initiatives within Spotify. Primarily, it guides the refinement of recommendation algorithms by providing insights into the accuracy of predictive modeling against actual user behavior. It also helps in evaluating the effectiveness of different music features in driving user engagement. The dashboard assists in understanding user preferences, which can inform marketing campaigns and content curation, ultimately aiming to improve user retention and the overall listening experience on the platform. By analyzing trends and prediction outcomes, the product teams can make informed decisions on feature development and enhance the personalization of user interactions.

## Access:
https://public.tableau.com/app/profile/diego.estuar/viz/SpotiFlowDiagnosticDashboard/SpotiFlowWeeklyWrapped

## Data Source(s):
User data is aggregated through Spotify's API, feeding into predictive algorithms for analysis.

## Key Metrics:
Predicted vs Actual Feature Similarity shows the difference in audio features between recommended songs and target song.
Audio Feature Time Series highlights change over time for Energy, Musicality, and Positivity by day.
Energy and Musicality Scores are based on aggregated audio features.
Positivity Score is based on valence audio features.
Listening Vibe reflects mood trends derived from valence data.
Weekly Listening and Top Songs are quantified to gauge user engagement levels.

## Define the metrics and explain any calculations.
Predicted vs Actual Feature Similarity
  - Predicted: Average audio feature % (averaged over 5 recommendations for given index)
  - Actual: Audio feature % for selected "Top Song" by index (1-5)
    
Energy Score
  - Weighted average of danceability, energy, and liveliness feature data
    
Musicality Score
  - Weighted average of acousticness and instrumentalness feature  data

Positivity Score
  - Valence score %
        
Listening Vibe
  - If the average valence feature data is:
        < 25%, "Is Everything Okay?"
        25% - 50%, "Slightly Sad"
        50% - 75%, "Feeling Great"
        > 75%, "A Little Too Happy"

Weekly Listening (mins/day)
  - Minutes listened by date
    
Weekly Top Songs
  - Count of total songs listened for date range
  - Positivity Score (valence %) for each song
    
## How to Use the Dashboard:
The dashboard is publically available and has several "drill down" features.
1. Click on a date to drill down and view listening analytics for that day.
2. Enter "Artist Name" or "Track Name" to drill down into more granular details.
3. Select "Top Song #" to track the similarity between prediction and actual song audio features based on the index selected.

## How to Refresh the Data:
Data can refresh live if connected to AWS database.
1. Fetch data from Spotify API
2. Python to AWS
3. AWS to Tableau Prep
4. Tableau Dashboard




In response to Spotify's "Wrapped" and its subsequent success and impact on engagement, we developed Spotiflow, a feature within the Spotify application aimed at allowing users to visualize their recent listening trends—dubbed their 'vibe'—and share these insights with friends.


The SpotiFlow weekly wrapped user dashboard was created to enhance the Spotify user experience by providing more personalized and frequent insights into users’ listening habits. By providing users with personalized analytics on a weekly basis, it caters to an audience that values understanding their music consumption patterns. This frequent, personalized insight helps users to see how their tastes evolve over time and encourages deeper interaction with the Spotify platform. The dashboard is designed for users who enjoy reflecting on their music choices, discovering trends in their listening habits, and sharing these insights with friends, thereby making the Spotify experience more engaging and communal.


The introduction of SpotiFlow's weekly wrapped dashboard is a strategic move to enhance user engagement with the Spotify platform. By allowing users to interact with their recent listening data at a detailed level, the dashboard makes the experience more relevant and personalized. This relevance is expected to increase user interaction with the platform, as users are likely to spend more time exploring their listening habits and discovering new music through personalized recommendations. The dashboard not only keeps users engaged but also encourages them to return to the platform regularly to check their latest insights, thereby increasing the frequency of engagement.


The dashboard plays a critical role in the business process of enhancing customer engagement. By providing weekly insights into listening habits, it keeps the platform dynamic and interactive. This ongoing engagement feeds into Spotify’s larger strategy of retaining users and increasing the time they spend on the platform. From a business perspective, the dashboard serves as a tool for collecting data on user preferences, which can then be analyzed to fine-tune recommendation algorithms, improving the overall user experience and satisfaction.


The SpotiFlow dashboard influences both user and business decisions. On the user side, insights from the dashboard can lead to decisions about exploring new genres, artists, or playlists based on their weekly listening vibes and top songs. This self-reflection on music preferences can enrich the user's listening experience and encourage the exploration of Spotify's vast library.

On the business side, SpotiFlow leverages the data gathered from user interactions with the dashboard to make decisions regarding predictive recommendations. By understanding patterns in listening habits, Spotify can tailor its music recommendations more accurately, thus enhancing the personalization of the user experience. This data-driven approach to recommendations supports Spotify's objective of being the most personalized music service, ensuring that users continually discover music that resonates with their tastes and moods.


https://public.tableau.com/app/profile/diego.estuar/viz/SpotiFlowUserDashboard/SpotiFlowWeeklyWrapped


User recent listening data retrieved from Spotify API using Python.


Energy Score
Musicality Score
Listening Vibe
Weekly Listening (# of Songs)
Weekly Top Songs
Total minutes listened


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



