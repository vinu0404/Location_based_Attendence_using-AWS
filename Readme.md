# Storenotify360

Storenotify360 is a project that aims to provide customers with notifications about sales and discounts when they enter a specific radius around a store. The project utilizes various AWS services to implement geofencing and notification capabilities.

## Project Overview

- Customers who are subscribed to receive notifications about sales and discounts from a particular store will get notification.
- A geofencing region is created around the store using a `geo.json` application.
- `AWS Tracker` only monitors  subscribed customers and detects when they enter the geofencing region not always tracks location.
- When a customer enters the geofencing region, an event is triggered using `AWS EventBridge`.
- The triggered event invokes a `Lambda function` that utilizes `AWS SNS` (Simple Notification Service) to send notifications to the subscribed customer.

## AWS Services Utilized

- **AWS Location Service**: Used to create and manage geofencing regions around the store using a `geo.json` application.
- **AWS Tracker**: Tracks the location of subscribed customers and detects when they enter the geofencing region.
- **AWS EventBridge**: Triggers events when customers enter the geofencing region.
- **AWS Lambda**: Contains the logic to handle the triggered events and send notifications using AWS SNS.
- **AWS SNS (Simple Notification Service)**: Responsible for sending notifications to subscribed customers when they enter the geofencing region.

  By leveraging these AWS services, Storenotify360 provides a seamless way for customers to receive timely notifications about sales and discounts when they are in the vicinity of a store, enhancing their shopping experience and increasing engagement with the store's offerings.
