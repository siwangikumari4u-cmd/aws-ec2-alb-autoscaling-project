# AWS Highly Available Web Application

## Project Overview

This project demonstrates a highly available and scalable web application architecture on AWS using:

- Amazon EC2
- Application Load Balancer (ALB)
- Auto Scaling Group (ASG)
- Amazon CloudWatch
- Amazon SNS
- Amazon Route 53

## Architecture

Users
|
Route53
|
Application Load Balancer
|
Auto Scaling Group
|
EC2 Instances

## Features

- Load balancing across multiple EC2 instances
- Automatic scaling based on CPU utilization
- CloudWatch monitoring
- SNS email notifications
- Route 53 DNS routing
- Multi-AZ deployment

## Auto Scaling Configuration

- Minimum Capacity: 2
- Desired Capacity: 2
- Maximum Capacity: 4
- Scaling Metric: CPU Utilization
- Target Value: 50%

## Monitoring

CloudWatch alarms trigger SNS notifications when CPU usage exceeds defined thresholds.

## Testing

Stress testing was performed using:

```bash
stress --cpu 4 --timeout 300
