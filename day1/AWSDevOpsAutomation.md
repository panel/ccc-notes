# AWS DevOps Automation
Sachin Dole

##  Automating Tvair

### Demo
- [server](https://tvarit.signin.aws.amazon.com/console)
- cccdemo
- devops123

### System Architecture
```
Clients -> LB -> EC2 -> (S3 | pg | external services)
```
Enterprise release patterns could take 1-8 person years

### Lessons Learned from Automation
- Automation is easy
- Automate in small increments
- Automate everything
- Release frequently
- Use automatic testing
- Don't roll your own infrastructure

Open sourced as [Tvarit](http://tvarit.io)

### Automating
- Whatever is messing around with automation requires IAM creds for AWS
- Services within your VPC will assume IAM roles
- Create a push button automation using API Gateway + Lambda

## DevOps Hot Takes
Use:
- Ingrastructure as cdoe
- Auto-scale, failover, monitoring
- CD

Avoid:
- Dedicated teams,
- Forms, emails to control.

### Determine non-value adding things
- testing
- build and release
- perf testing

### Focus on Value Adding Activities
- Business Requirements Analyses
- Software Product Develop

> Up to 40% gains realized by automating tasks/CD

### Soft Side
- Cloud native
- CALMS
  - Cultuer
  - Automation
  - Lean
  - Measured
  - Security

### Costs
- Given already paying for AWS, automation doesn't present an additional cost
- Many things are provided as part of the platform
