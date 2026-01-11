# Scalable Web Application Deployment – ALB and Auto Scaling

In this project, I deployed a scalable web application using an Application Load
Balancer and an Auto Scaling Group.

## What I did

1. I created a launch template using Amazon Linux.
2. I added a user data script to automatically install and start Apache.
3. I created a target group for the load balancer.
4. I created an Application Load Balancer in two Availability Zones.
5. I created an Auto Scaling Group using the launch template.
6. I attached the Auto Scaling Group to the target group.
7. I configured health checks so unhealthy instances are replaced automatically.
8. I tested the setup by accessing the ALB DNS name in a browser.

## User data script

```bash
#!/bin/bash
yum update -y
yum install httpd -y
systemctl start httpd
systemctl enable httpd
echo "<h1>Welcome to the Scalable Web App</h1>" > /var/www/html/index.html
