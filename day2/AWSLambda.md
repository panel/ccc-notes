# AWS Lambda

http://slideshare.net/derekashmore

## Overview

- Supports Java, Node.js, and Python
- AWS mangages hardware, scaling, maintenance
- Event driven
- Stateless

## Events

- Can come from:
  - API gateway
  - scheduled
  - storage writes
  - lots of other stuff
  
## Features

- Unlimited parallelism
- Don't pay for idle
- Lower CPU cost (but this is not guaranteed in the future)
- No need for O/S upgrades, backups
- Less control and no fine tuning
- No pooling, caching, session
- Proprietary interface is a significant downside

## Request Handlers

- Inputs:
  - Event
  - Context:
    - request ID
    - Fn name, ARN, version
    - Cognito identity
- Output:
  - user defined
  
## Deployment

- From Zip Artifact

## Env

- Java 8
- AWS SDK for Node.js (> v4)
- Make sure to create/destroy your connections

## Versioning

- Deployed Lambdas are uniquely versioned and unchangeable
- Aliases for PROD, TEST, DEV can be moved
- Need to correlate source control with deployed lambdas
- Recommneded to tag with lambda version

## Debug

- No remote debug
- Log to console

## Config

- Config in zip file

## Performance

- Java and Node.js are about even in performance

## Microservice Arch

- Don't expose to public traffic
- Use gateway API

## Competitors

- Google and Azure have announced competitors but they're not up to snuff
