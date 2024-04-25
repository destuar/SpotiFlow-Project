# SpotiFlow Diagnostic Dashboard
Purpose:
Designed as an internal tool for Spotify, the SpotiFlow Diagnostic Dashboard offers comprehensive analytics on user listening behavior and model prediction accuracy. Unlike "Wrapped," which is consumer-facing, this dashboard provides Spotify with in-depth insights, fostering data-driven decision-making to refine user experience and model performance.

Audience:
This dashboard is for Spotify's analytics and product teams. It equips them with detailed listening data and the precision of predictive modeling, enabling targeted improvements and personalized user experiences.

Addressing the Business Challenge:
The dashboard aids in identifying engagement trends and evaluating model predictions, crucial for iterating on Spotify's recommendation engine. Enhanced prediction accuracy can elevate user satisfaction and retention, directly impacting Spotify's market position.

Business Process Integration:
The dashboard is pivotal in analyzing user engagement and predicting trends. These analytics inform strategic decisions in marketing and content curation, enhancing user stickiness to the platform.

Decision Influence:
Data from the dashboard steers both algorithm refinements and user engagement strategies. For users, it may influence music exploration, while for Spotify, it shapes content recommendation and user interface enhancements.

Dashboard Access:
For internal stakeholders, access will be provided through the corporate intranet.

Data Source:
User data is aggregated through Spotify's API, feeding into predictive algorithms for analysis.

Key Metrics and Definitions:
Energy and Musicality Scores are based on aggregated audio features.
Listening Vibe reflects mood trends derived from valence data.
Weekly Listening and Top Songs are quantified to gauge user engagement levels.
Usage Guide:
Internally accessible, the dashboard offers filters and sliders for dynamic data exploration by date, user segments, and other relevant dimensions.

Data Refresh Protocol:
Data is periodically updated through a pipeline from Spotify's API to AWS, and then into Tableau Prep for dashboard synchronization.
