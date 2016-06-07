# Patterns for DevOps and CD
Danilo Sato (@dtsato) Thoughtworks

## The Day We Failed Our Deployment
- Agile software development delivering code every two weeks
- Business nervous, required releases during outage windows
- Manual process, knowledge lives with one person.
- Search indexed on staging data. Smoke test passed.
- Business demo'd search and it done blew up

### How to Solve the Problem (the wrong way)
- More process
  - additional ceremony/barrier to delivery
- Deployment frequency decreases
- Amount of changes increase for each deploy
- More change introduces more risk
- Leads to more process

### A Different Way
- Document the release process and identify pain points
- Was able to facilitate technical review of the process
  - found redundant steps
  - found pieces to automate
  - came up with story/epics to improve Deployment
- Negotiated with client in order to add stories to iterations
- Improved release process and removed pain

### With DevOps
- Process is automated
- Deployments are more frequent
- Smaller diffs
- Lower risk on each deployment

> Our goal is to make deployment a "non-event"

## Automation

```
Idea
  Code
  Tests
  Package
  Servers/Env
  Exploratory Testing/UAT/Approval
  Deploy
Production
  Monitoring
  Alerts
  Support
  Data/Analytics
  User Feedback
  Insights
Idea
```
- Idea -> Production = cycle time.
- Cycle Time is inversely related to Quality

### Deployment Pipeline
- Every commit should be production ready
- Fastest feedback go earlier in the Pipeline
- Slower feedbacks go later
- Publish to repository after fast tests
- Include VCS and Repository as targets

### Principle for Reducing Deployment Risk

#### Incremental Is Better Than "Big Bang"
- More changes means more risk
- Slower feedback cycle
- Cannot learn from code already completed
- Handling failure is much more complex

#### Deploy != Release
Decouple the deployments (code in production) from release (available to users)

#### Focus on Delivering Small Batches
- Mean Time Between Failure
  - Focuses on preventing failures from happening
  - Assumes failures are preventable
- Mean Time To Recover
  - Focuses on facilitating positive changes
  - Acknowledges failures happen

#### Building Quality In
- Provide a safety net to developers so that they can build features quickly
- Embrace a culture of failing fast and iterating

### Parallel Change
  1. Expand: add new API
  2. Migrate collaborators
  3. Contract remove old API

- Push out new features parallel to existing features
- As new features become ready, shift users to new feature
- Contract old feature
- Works for changing architecture/db

### Blue-Green Deployments
- Deploy new version completely on a parallel env.
- Once change is proven, reroute to the new env.
- What about the database?
  - Decouple the changes
  - Deploy application code quickly
  - Deploy database code more slowly
  - Requires database to be both backwards and forward compatible

### Canary Release
- Like blue-green, but only route a fraction of users to new version
- Eventually get 100% traffic on the new version and kill the old version

### Feature Toggles
- Decouples release from deployments
- [Martin Fowler on Feature Toggles](- http://martinfowler.com/articles/feature-toggles.html)

### Dark Launching
- Enables testing in production
- Finds more edge cases

### Phoenix Servers
- Snowflake Server
  - Unique
  - Evolves as users jump in and make changes
  - Difficult to figure out reasoning behind current state
- Phoenix Server
  - All changes defined in code
  - Additional changes can be applied in code
  - You can kill the server and apply the diff
  - Uses chef/ansible/salt/puppet

### Immutable Servers
- Infrastructure components do not change.
- Servers and boxes get thrown away and new one is published
- AMI as an artifact/Container as an artifact.
