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

- **Pitch Features**
    - `pitch_type`: The type of pitch that was thrown and hit for a home run
        - `CH : Changeup`
        - `CU : Curveball`
        - `EP : Eephus`
        - `FC : Cut Fastball (Cutter)`
        - `FF : Four-seam Fastball`
        - `FO : Pitch Out`
        - `FS : Sinking Fastball / Split-Fingered (Splitter)`
        - `FT : Two-seam Fastball`
        - `KC : Knuckle-curve`
        - `KN : Knuckleball`
        - `SC : Screwball`
        - `SI : Sinker`
        - `SL : Slider`
    - `p_throws`: the strong hand in which the pitcher threw the pitch
    - `pfx_x`: the horizontal movement, in inches, of the pitch between the release point and home plate, as compared to a theoretical pitch thrown at the same speed with no spin-induced movement. This parameter is measured at y=40 feet regardless of the y0 value.
    - `pfx_z`: the vertical movement, in inches, of the pitch between the release point and home plate, as compared to a theoretical pitch thrown at the same speed with no spin-induced movement. This parameter is measured at y=40 feet regardless of the y0 value.
    - `vx0`: the velocity of the pitch, in feet per second, in three dimensions, measured at the initial point.
    - `vy0`: the velocity of the pitch, in feet per second, in three dimensions, measured at the initial point.
    - `vz0`: the velocity of the pitch, in feet per second, in three dimensions, measured at the initial point.
    - `ax`: the acceleration of the pitch, in feet per second per second, in three dimensions, measured at the initial point.
    - `ay`: the acceleration of the pitch, in feet per second per second, in three dimensions, measured at the initial point.
    - `az`: the acceleration of the pitch, in feet per second per second, in three dimensions, measured at the initial point.
    - `effective_speed`: the (actual) speed of the pitch upon the ball crossing home plate
    - `release_speed`: the (perceived) speed of the pitch upon release from the pitcher
    - `release_spin_rate`: how much spin, in revolutions per minute, a pitch was thrown with upon release.
    - `release_extension`: how far off the mound, in feet, a pitcher releases the pitch.
    - `release_pos_y`: the release coordinates in three dimensions, measure at the initial release point.
    - `release_pos_x`: the release coordinates in three dimensions, measure at the initial release point.
    - `release_pos_z`: the release coordinates in three dimensions, measure at the initial release point.
- **MLB Features**
    - `game_year`: the season the home run hit occurred (2015, 2016 and 2017).
    - `weight_(oz)`: the weight of the baseballs in oz from each season (2015, 2016 and 2017).
    - `circumference_(in)`: the circumference of the baseballs in inches from each season (2015, 2016 and 2017).
    - `avg_seam_height`: seam height was defined as the average radial distance from the seam to the ear, 3 mm left and right of the seam.
    - `avg_ccor`: cylindrical coefficient of restitution (ccor) is the measurement of the "bounciness" of the baseball and is the core ingredient of "the pill" the middle rubber of the baseball.
    - `avg_ds`: a measure of a ball's hardness. Its measurement is conducted to represent bat-ball impact forces.
- **Batter Features**
    - `player_name`: the name of the player that hit the home run
    - `height`: the height in inches of the player that hit the home run
    - `weight`: the weight in lbs of the player that hit the home run
    - `age`: the age of the player that hit the home run
    - `hit_distance_sc`: the distance the ball traveled from home plate
    - `launch_speed`: **(Target Variable)** aka exit velocity, measures the speed (mph) of the baseball as it comes off the bat, immediately after a batter makes contact.
    - `launch_angle`: how high, in degrees, a ball was hit by a batter.
    - `bb_type`: the type of hit that came off the bat (fly ball or line drive) for a home run.
    - `sz_top`: the distance in feet from the ground to the top of the current batter’s rulebook strike zone as measured from the video by the PITCHf/x operator. The operator sets a line at the batter’s belt as he settles into the hitting position, and the PITCHf/x software adds four inches up for the top of the zone
    - `sz_bottom`: the distance in feet from the ground to the bottom of the current batter’s rulebook strike zone. The PITCHf/x operator sets a line at the hollow of the knee for the bottom of the zone.
    - `zone`: the location of the pitch as is crossed home plate according to the mapped areas of the batters zone box (1 - 14).
    - `plate_x`: strike zone coordinate x
