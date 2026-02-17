# WEC 2021 Analysis
This project focuses on the Hypercar Class of the 2021 WEC Championship with analysis performed between the teams for each race of the season. The goal is to extract performance, consistency, and strategic insights that are crucial to motorsport engineers, strategists, and analysts.

The data was utilized from kaggle. The data was then filtered to only give me the 2021 season.

Link: https://www.kaggle.com/datasets/tristenterracciano/fia-wec-lap-data-20122022 

The visualizations were done by utilizing the plotly library. Their website helped me alot in doing this project.

Link: https://plotly.com/python/

To explore the interactive visualizations, please download the code and run it locally.

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

### Driver-Level Consistency View
Plot Type: Line plot with markers (faceted by team)

Axes:
- X-axis: Lap number
- Y-axis: Lap time in seconds
- Color: Driver name
- Line group: Driver stint
- Facets: One panel per team

What does this plot show: This plot highlights the lap by lap consistency patterns of each stint individually which makes it easier to compare pace and performance across different drivers within teams

Key Insights:
- Proper separation between stints helps in avoiding misleading trends
- Allows evaluation of intra-stint consistency
- Highlights how pace resets after pit stops or driver changes
- Easy teammate comparisons within the same car

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

### Stint Degradation: Start vs End Pace
Plot Type: Line Chart

Axes:
X-axis: Lap number (start and end of each stint)
Y-axis: Average Lap Time (s)
Line: Team number
Color: Driver Stint

What does this plot show: Each line represents a single driver stint, connecting the average pace of the first 3 laps to the average pace of the last 3 laps, allowing direct visual comparison of how pace changes over the course of that stint. Only stints with 5+ laps are included for meaningful analysis

Key Insights:
- Upward slope meaning that lap time increased by the end of the stint(degradation)
- Flat or downward slope indicating a consistent or improving pace
- Steeper slopes indicate stronger degradation effects

Motorsport Value:
- Provides a clear start to end comparison without lap by lap noise
- Helps engineers evaluate how risky a stint is in terms of pace
- Supports decisions on optimal stint length and driver deployment

### Tire Degradation Rate vs Stint Length
Plot Type: Scatter plot with OLS trendlines

Axes:
- X-axis: Stint length (laps)
- Y-axis: Degradation rate (seconds per lap)
- Color: Team number
- Trendlines: One per team (OLS regression)

What does this plot show: Each point represents one stint's degradation rate, calculated using linear regression on all laps within that stint. The degradation rate shows how many seconds per lap the car slows down (positive) or speeds up (negative). Team-specific trendlines reveal whether longer stints hurt or help each team.

Key Insights:
- Positive values: Pace loss during stint (tire degradation)
- Negative values: Pace gain during stint (fuel burn-off effect)
- Downward trendline: Team performs better on longer stints
- Upward trendline: Team degrades more on longer stints
- Flat trendline: Stint length doesn't affect degradation
- Different teams show different patterns, revealing strategic differences

Motorsport Value:
- Optimal stint length decisions
- Risk assessment for extending stints

## Gap Evolution to Leader:
Plot Type: Multi Line Chart

Axes:
- X-axis: Lap number
- Y-axis: Gap to race leader (seconds)
- Color: Team number

What does this plot show: This plot displays how the time gap between each team and the race leader evolves lap by lap throughout the race.

Key Insights:
- Identifies when and where races are won or lost
- Shows which teams can recover after setbacks

Motorsport Value:
- Evaluate race control and recovery ability
- Understand competitive phases within a race
- Support post race debriefs and strategy simulations

## Driver Pace Delta within Team and Team Pace Delta

### Driver Pace Delta within Team
Plot Type: Box plot

Axes:
- X-axis: Driver which is grouped by team number
- Y-axis: Lap time delta(seconds)
- Color: Driver name

What does this plot show: This plot compares driver pace within the same team. Each lap time is measured against the average of the first 3 laps of that driver's stint (baseline). Only laps after the baseline period (lap 4+) are analyzed.

Key Insights:
- Tighter box indicating driver is more consistent
- Lower median indicating faster driver

Motorsport Value:
- Driver performance evaluation
- Reveals aggressive versus conservative driving styles
- Data-backed comparisons during driver debriefs

### Team Pace Comparison (Lap Time Δ vs Stint First Lap)
Plot Type: Violin plot

Axes:
- X-axis: Team number
- Y-axis: Lap time Δ vs baseline (seconds)
- Color: Team

What does this plot show: This plot compares overall team pace. Like the driver analysis, each lap is measured against the average of the first 3 laps of each stint. All drivers' data is combined per team, and all laps are included

Key Insights:
- Narrow violins means consistent race pace
- Wide violins means high variability
- Skewed distributions means aggressive or conservative strategies
- Median and quartiles show typical degradation patterns

Motorsport Value:
- Comparing overall team performance
- Identifying consistency advantages
- Helps in strategy and technical debriefs

## Notes
- Baseline Calculation: Throughout this analysis, "baseline pace" refers to the average lap time of the first 3 laps of each stint (laps 0, 1, 2). This provides a starting reference that smooths out outliers from individual laps.
- All analyses include all racing data with outliers retained to show true race conditions and hidden patterns. Extreme values represent traffic, incidents, and exceptional performance moments.
