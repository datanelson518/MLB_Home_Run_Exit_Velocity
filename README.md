# MLB Home Run Exit Velocities 2015 vs 2017

*Jon Nelson*

---

## Problem Statement

Using the physical data about baseballs combined with the personal and game statistics for each player that hit a home run, between the years of 2015 and 2017, I will use regression modeling to predict the exit velocity of each home run hit. Using the predicted values I will draw a conclusion about the changes made to baseballs to determine if their is an influence on exit velocities from "juiced" baseballs.

---

## Data Dictionary

### Statcast Search

`pitch_type`
`game_date` (make index)
`release_speed`
`release_pos_x`
`release_pos_z`
`player_name`
`batter` (drop)
`pitcher` (drop)
`events` (drop)
`description` (drop)
`spin_dir` (drop)
`spin_rate_deprecated` (drop)
`break_angle_deprecated` (drop)
`break_length_deprecated` (drop)
`zone`
`des` (drop)
`game_type` (drop)
`stand` (drop)
`p_throws`
`home_team`
`away_team`
`type` (drop)
`hit_location` (drop)
`bb_type`
`balls` (drop)
`strikes` (drop)
`game_year`
`pfx_x`
`pfx_z`
`plate_z` (drop)
`on_3b` (drop)
`on_2b` (drop)
`on_1b` (drop)
`outs_when_up` (drop)
`inning` (drop)
`inning_topbot` (drop)
`hc_x` (drop)
`hc_y` (drop)
`tfs_deprecated` (drop)
`tfs_zulu_deprecated` (drop)
`fielder_2` (drop)
`umpire`
`sv_id` (drop)
`sz_top`
`sz_bottom`
`hit_distance_sc`
`launch_speed`
`launch_angle`
`effective_speed`
`release_spin_rate`
`release_extension`
`game_pk`
`pitcher.1` (drop)
`fielder_2.1` (drop)
`fielder_3` (drop)
`fielder_4` (drop)
`fielder_5` (drop)
`fielder_6` (drop)
`fielder_7` (drop)
`fielder_8` (drop)
`fielder_9` (drop)
`release_pos_y`
`estimated_ba_using_speedangle` (drop)
`estimated_woba_using_speedangle` (drop)
`woba_value` (drop)
`woba_denom` (drop)
`babip_value` (drop)
`iso_value` : batters raw power (Isolated Power)
`launch_speed_angle`
`at_bat_number` (drop)
`pitch_number` (drop)
`pitch_name`
`home_score` (drop)
`away_score` (drop)
`bat_score` (drop)
`fld_score` (drop)
`post_away_score` (drop)
`post_home_score` (drop)
`post_bat_score` (drop)
`post_fld_score` (drop)
`if_fielding_alignment` (drop)
`of_fielding_alignment` (drop)

### Stadium

### Player Personal Stats

### Baseballs
