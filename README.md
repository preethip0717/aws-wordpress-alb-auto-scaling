*WordPress Deployment on AWS with Load Balancing and Auto Scaling

*Project Overview

This project demonstrates deploying a WordPress website on Amazon Web Services (AWS) using EC2, an Application Load Balancer (ALB), and an Auto Scaling Group (ASG).

The goal was to configure a reusable web server image, distribute HTTP traffic across multiple EC2 instances, and practice replacing instances through Auto Scaling.

*AWS Services Used

- Amazon EC2 — Hosts the WordPress web server.
- Amazon Machine Image (AMI) — Stores a reusable instance image.
- Launch Template — Defines the configuration for launching EC2 instances.
- Application Load Balancer (ALB) — Distributes incoming HTTP traffic.
- Target Group — Registers instances and monitors their health.
- Auto Scaling Group (ASG) — Maintains two EC2 instances across Availability Zones.

*Technologies

- Amazon Linux 2023
- Nginx
- PHP and PHP-FPM
- MariaDB
- WordPress

*Implementation Steps

1. Launched an EC2 instance and installed Nginx, PHP, and MariaDB.
2. Configured the database and deployed WordPress.
3. Created an AMI from the configured WordPress server.
4. Created a Launch Template using the WordPress AMI.
5. Created a target group with HTTP health checks.
6. Configured an internet-facing Application Load Balancer.
7. Created an Auto Scaling Group across two Availability Zones.
8. Verified that the WordPress website was accessible through the ALB DNS name.
9. Replaced EC2 instances and verified that the new instances used the correct AMI.

*Architecture

Internet → Application Load Balancer → Target Group → EC2 Instances managed by Auto Scaling Group

*what I Learned

- Deploying a web application on Linux.
- Configuring Nginx, PHP, and MariaDB.
- Creating and using AMIs and Launch Templates.
- Configuring load balancing and target health checks.
- Managing EC2 instances through Auto Scaling.
- Troubleshooting database connectivity and Launch Template version issues.

*Limitations

The WordPress database is stored locally on each instance. The instances do not share a central database or synchronize WordPress content. A production-ready high-availability architecture would require shared database and media storage.

*Project Status

Completed as a hands-on AWS learning project.



