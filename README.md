# Scalable Web Application – ALB and Auto Scaling

In this project, I deployed a highly available and scalable web application
using Amazon EC2, an Application Load Balancer (ALB), and Auto Scaling.

This setup allows the application to automatically scale based on traffic
and remain available even if individual instances fail.

## AWS Services Used
- Amazon EC2
- Application Load Balancer (ALB)
- Auto Scaling Group
- Amazon VPC
- CloudWatch

## What I built
- A launch template for EC2 instances
- An Auto Scaling Group across multiple Availability Zones
- An Application Load Balancer to distribute traffic
- Health checks and automatic instance replacement

