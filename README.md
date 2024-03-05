# ProjectK
Overwatch League Data Analysis & Machine Learning

## Project Overview
As a long-term Overwatch enthusiast with a deep passion for gaming, I selected this project for my ISBA 4715 class, treating it more as a passion project than merely a school assignment. I embarked on this venture by extracting data from Battle.Net's and Twitch's APIs, focusing on various metrics such as Overwatch League (OWL) team win rates and Twitch video or stream viewership, among others. Following the data extraction, I proceeded to upload the dataframes to my AWS database, configuring them with MySQL. This led to the creation of 10 tables, some boasting over 400+ rows. My goal was to analyze the data to identify strategies that could enhance Overwatch's gameplay, which, combined with market trend research, was aimed at boosting player engagement and satisfaction.

## Data
### Source
The data is extracted from Battle.net's API to get Overwatch League data and from Twitch's API to get Overwatch video/streams data. I've also taken in a table from kaggle which is Overwatch League's 2018 data so I can compare the 2022 and 2018 stats.

### Characteristics
The data extracted resulted in 10 different tables, these are the list of tables and columns:

1. **Heroes**,
Columns:
heroes
heroDamageDone
damageTaken
finalBlows
eliminations
deaths
ultsUsed
ultsEarned
timePlayed
healingDone
soloKills

2. **Teams**, 
Columns:
TeamID
name
code
logo
icon
competitions
roster
primaryColor
secondaryColor

3. **games**,
Columns:
gameID
matchID
map
maptype
guid

4. **match_map_stats** (This is the 2018 stats I took from kaggle),
Columns:
round_start_time
round_end_time
stage
match_id
game_number
match_winner
map_winner
map_loser
map_name
map_round
winning_team_final_map_score
losing_team_final_map_score
control_round_name
attacker
defender
team_one_name
team_two_name
attacker_payload_distance
defender_payload_distance
attacker_time_banked
defender_time_banked
attacker_control_perecent
defender_control_perecent
attacker_round_end_score
defender_round_end_score
mms_ID

5. **matches**,
Columns:
matchID
winner
team1
team2
team1score
team2score
startTimestamp
actualStartTimestamp
actualEndTimestamp
competitionId
seasonId
localTimeZone

6. **players**,
Columns:
player_id
given_name
roles
TeamID
competitions
familyName

7. **streams_twitch**,
Columns:
streamid
user_id
user_name
game_id
game_name
type
title
viewer_count
started_at
language
thumbnail_url
S_ID

8. **tags_streams_twitch**,
Columns:
stream_id
tags
tags_ID

9. **top_games_twitch**,
Columns:
game_id
name
box_art_url
igdb_id

10. **videos_twitch**,
Columns:
video_id
stream_id
user_id
user_login
user_name
title
created_at
published_at
url
thumbnail_url
viewable
view_count
language
type
duration
muted_segments

## Notebooks
### SQL & R Analysis
In this notebook, I conducted a complete data analysis by processing the data from a database and utilizing it to build machine learning regression models (such as random forest, linear, and gradient) in order to generate predictive models.

### Data Collection
In these notebooks, I'm extracting the data from Battle.net and Twitch's API 

## Further Improvements
I think my database is a bit too small to analyze and make conclusions of a game with an extremely large playerbase, for example, making a solution from 300 twitch videos shouldn't be enough, and I should be analzying about 2000+ records. This applies to the battle.net data too, my analysis would be a good starter point or template for a larger scale analysis, but with a small number of records, it's best to not make conclusions from my solutions.
