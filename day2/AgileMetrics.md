# Agile Metrics: Velocity is NOT the goal
Doc Norton

## What's Velocity?
- work units / time
- units of value / time?
- it's a lagging indicator. looking back
  - not a good short term predictor
  - good for viewing patterns over longer contexts
  - focusing on "solving" velocity leads to treating symptoms
- measure of a complex system
  - analogy: body weight
    - lagging indicator of complex system
    - lots of factors that go into body weight
    - not able to make a health determination based on weight alone
  - devoid of detail. cannot describe health of team as a number

## A Tale of Two Velocities
- [10, 11, 9, 10]
  - (weather based) 10
  - (rolling avg) 10
  - (stdDev) 0.7
  - (68% confidence) 9.3 - 10.7
  - (95% confidence) 8.4 - 11.4
- [7, 14, 6, 10]
  - (weather based) 10
  - (rolling avg) 10
  - (stdDev) 3.1
  - (68% confidence) 6.9 - 13.1
  - (95% confidence) 3.8 - 16.2

Using velocity + stdDev you can create a burn down chart that's ranged with 68% confidence or 95% confidence

## The Need for Speed
- We expect agile teams to get faster
- Stakeholders artificially ask for more magical velocity points in order to hit deadlines.

### The Hawthorn Effect
- When you observe something, the observation can impact performance.
- That which is measured and is reported on will improve… at a Cost

### Goodhart's Law
- Any observed statistical regularity will tend to collabpse when pressure is placed upon for control purposes
- When a measure become a target, it ceases to be a good measure
- The team will modify all aspects of what they did in order to achieve the goal
- Leads to perverse incentives

> What matters is not setting quantitive goals but fixing the method by which these goals are attained.

Attack the root causes of velocity rather than trying to manipulate velocity directly.

## What Causes Variable Velocity?
- time poorly spent: focus on CYA work in lieu of value add
- dependency on other teams
- poor story composition
- messy code
- too much work in progress

## How To Find Causes/Corellations

### Scatter Diagrams
- x: complexity (cyclomatic), y: velocity
  - negative correlation
  - use as an argument to invest in tech debt
- x: value (PO revenue estimation), y: velocity
  - ambiguous correlation
  - prioritizing by value without tech contribution leads to strife around unrecognized technical dependencies
- x: code coverage, y: velocity
  - positive correlation
  - test your junk!
- x: story size, y: lead time
  - lead time: amount of time between idea and production
  - positive correlation
  - decompose larger stories down into more manageable chunks
  - even though many small stories may be more points, it can lead to higher throughput
- [Friedman's Thermostat](http://justinhohn.typepad.com/blog/2013/01/milton-friedmans-thermostat-analogy.html)
  - you can't make assumptions based on correlations alone
  - look for confounding variables

### Cumulative Flow
- total tasks or total complexity in each phase over time (daily)
- allows a quick view of how the team is progressing
- able to quickly identify bottle necks in the process
- add additional lanes as needed to identify more subtle bottlenecks. then remove additional lanes

### Measure Many Things
- Add code love as part of your commit as a proxy for satisfaction
- Mercury app for lipert scale for daily feedback. distances itself from the work

## Additional Visualizations
- Distribution chart by lead time.

## Metrics are for Teams Not Managers
