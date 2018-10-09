# Major League Baseball Home Run Exit Velocities

*Jon Nelson*

---

## Description

One of the most recent developments in MLB is the debate about why more home runs were hit in the 2017 season than any other season in the leagues history. More home runs were hit in the 2017 season than when the record for home runs hit was broken during the steroid era and many people want to know how this can be. One specific area for investigation is related to the most important item to the game, the baseball. During the 2017 season there were numerous complaints from major league pitchers that the ball felt different and the overall result was a record breaking year.

Thanks to Baseball Savant and all the different baseball statistics that are tracked on every pitch we can start to analyze if there is any connections between the baseballs being used and the increase in home runs. Specifically, I plan to draw a conclusion about whether or not the change seen in baseballs between the 2015, 2016 and 2017 MLB seasons has influenced a batters home run exit velocity.

Using machine learning techniques I will build multiple regression models in order to predict a specific batters home run exit velocity on a particular pitch. After running these models I will decide which model should be used as the production level model and examine the influences of each feature that is provided. This model will provide the necessary insight into if a batters exit velocity is influenced by the baseballs being used along with providing further insight into what is influencing a batters exit velocity.

---

## Problem Statement

Using the physical data about baseballs combined with the personal and game statistics for each player that hit a home run, between the years of 2015 and 2017, I will use regression modeling to predict the exit velocity of each home run hit. Using the predicted values I will draw a conclusion about the changes made to baseballs to determine if their is an influence on exit velocities from "juiced" baseballs.

---

## Data Dictionary

---

### Statcast Search

- `pitch_type`
- `game_date` (make index)
- `release_speed`
- `release_pos_x`
- `release_pos_z`
- `player_name`
- `batter` (drop)
- `pitcher` (drop)
- `zone`
- `p_throws`
- `home_team`
- `away_team`
- `bb_type`
- `game_year`
- `pfx_x`
- `pfx_z`
- `plate_z` (drop)
- `hc_x` (drop)
- `hc_y` (drop)
- `sz_top`
- `sz_bottom`
- `hit_distance_sc`
- `launch_speed`
- `launch_angle`
- `effective_speed`
- `release_spin_rate`
- `release_extension`
- `release_pos_y`
- `launch_speed_angle`
- `pitch_name`

### Stadium

### Player Personal Stats

### Baseballs
