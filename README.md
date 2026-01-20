# WEC-2022-Analysis
This project focuses on the Hypercar Class of the 2021 WEC Championship with analysis performed between the teams for each race of the season. The goal is to extract performance, consistency, and strategic insights that are crucial to motorsport engineers, strategists, and analysts.

## Driver Stint Consistency
This analysis is presented by using 2 line plots:

### Team Consistency View
Plot Type: Line plot with markers

Axes:
- X-axis: Lap number
- Y-axis: Lap time in seconds
- Color: Team number
- Line group: Driver stint

What does this plot show: This plot highlights the lap-by-lap consistency patterns at the team level, making it easy to compare how different teams manage pace across the race

Key Insights:
- Stable, flat traces indicate strong consistency
- Spikes corresponding to the pit laps, traffic, or incidents
- Variations between teams tells us how each crew manages tire life, pace, and on track situations throughout the race

### Stint-Specific Consistency View
Plot Type: Line plot with markers

Axes:
- X-axis: Lap number
- Y-axis: Lap time in seconds
- Color: Driver stint
- Line group: Team number

What does this plot show: This plot highlights the lap by lap consistency patterns of each stint individually which makes it easier to compare pace and degradation across differnt stints

Key Insights:
- Proper separation between stints helps in avoiding misleading trends
- Allows evaluation of intra-stint consistency
- Highlights how pace resets after pit stops or driver changes

### Motorsport Value
- Team wide behavior
- Stint level behavior
- Using both of these views shows us how teams review race data, first at a broad level then stint level

## Pit Stop Strategy Effectiveness
Plot Type: Step line plot with pit stop markers

Axes:
- X-axis: Lap number
- Y-axis: Lap time in seconds
- Color: Team number
- Markers: Pit stop laps

What does this plot show: This plot highlights how lap times change before and after a pit stop which helps us to evaluate pit timing and its impact on the performance

Key Insights:
- Identifies which teams gained or loss time through pit timing
- Highlights the effictiveness of the undercut or overcut strategies

Motorsport Value
- Helps in modelling undercut or overcut strategies to be used in future races
- Helps to evaluate when to make decisions relating to pit stop timing

## Stint Length vs Degradation
This analysis is presented by 3 plots:

### Stint Length vs Lap Time Degradation (Delta vs First Lap)
Plot type: Heatmap

Axes:
- X-axis: Lap number
- Y-axis: Driver stint
- Color: Lap time delta vs first lap of the stint

What does this plot show: 
