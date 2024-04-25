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
