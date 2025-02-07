## Automating Notifications for Future-Dated Amazon EC2 Capacity Reservation State Changes

## Overview
AWS customers are able to proactively reserve [future-dated Amazon EC2 On-Demand Capacity Reservations (known as future-dated CRs)](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/capacity-reservations-create.html#create-future-cr) to get capacity assurance for workloads and events. This CloudFormation template enables automated notifications for future dated Amazon EC2 Capacity Reservations. 

### Configuration Parameters
-	Email Address: Specify one or more email addresses to receive notifications about your future-dated CRs.
-	CapacityReservationId : Provide the ID of the future-dated CRs you want to monitor.
-	MonitoredStates: Select the states you want to track, such as failed, expired and cancelled.

## Resources Created
The template automatically creates and configures:
-	An Amazon SNS topic for notification delivery 
-	An Amazon EventBridge rule that monitors your specified future-dated CR's states
-	The necessary IAM permissions and configurations

## Setup Instructions
1. Deploy the CloudFormation template
2. Check your email for subscription confirmation
3. Click the confirmation link to activate notifications
4. Start receiving automated alerts for state changes

## Important Notes
-	After deployment, each specified email address will receive a subscription confirmation email
-	Recipients must click the confirmation link in the email to start receiving notifications
-	The notifications will trigger whenever your future-dated CR enters any of the specified states

## Benefits
- Real-time monitoring of future-dated CRs.
- Automated notification system

## License
This template is licensed under the MIT-0 License. See the LICENSE file.

