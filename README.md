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
Plot Type: Step line chart with pit stop markers

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

## Stint Degradation
This analysis is presented by 2 plots:

### Stint Degradation: Start vs End
Plot type: Line Chart

### Stint Degradation vs Stint Length
Plot type: Scatter Plot

## Gap Evolution to Leader:
Plot type: Multi Line Chart

## Driver Pace Delta within Team and Team Pace Delta

### Driver Pace Delta within Team
Plot type: Box plot

### Team Pace Comparison (Lap Time Δ vs Stint First Lap)
Plot Type: Violin plot

Axes:
- X-axis: Team number
- Y-axis: Lap time delta

What does this plot show: The full distribution of lap time deltas for each team

Key Insights:
- Narrow violins means consistent race pace
- Wide violins means high variability
- Skewed distributions means aggressive or conservative strategies

Motorsport Value:
- Comparing overall team performance
- Identifying consistency advantages
- Helps in strategy and technical debriefs
