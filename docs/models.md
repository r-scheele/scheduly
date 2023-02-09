# Data models
Features

1. Dynamic Scheduling:

    ## EC2 Instances

    | Column Name | Data Type | Description |
    | --- | --- | --- |
    | ID | Integer | Primary Key |
    | Region | String | AWS region where the instance is located |
    | Instance Type | String | Type of EC2 instance |
    | State | String | Running or Stopped |
    | Launch Time | Datetime | Time when the instance was launched |
    | Termination Time | Datetime | Time when the instance was terminated |


    ## Traffic Data

    | Column Name | Data Type | Description |
    | --- | --- | --- |
    | Timestamp | Datetime | Timestamp of the traffic data |
    | Request Count | Integer | Number of requests at the timestamp |
    | Error Count | Integer | Number of errors at the timestamp |


2. Multi-Region Scheduling:

    ## EC2 Instances

    | Column Name | Data Type | Description |
    | --- | --- | --- |
    | ID | Integer | Primary Key |
    | Region | String | AWS region where the instance is located |
    | Instance Type | String | Type of EC2 instance |
    | State | String | Running or Stopped |
    | Launch Time | Datetime | Time when the instance was launched |
    | Termination Time | Datetime | Time when the instance was terminated |

    ## AWS Regions

    | Column Name | Data Type | Description |
    | --- | --- | --- |
    | Name | String | Name of the AWS region |
    | Availability | String | Available or Unavailable |


3. Predictive Scheduling:

    ## EC2 Instances

    | Column Name | Data Type | Description |
    | --- | --- | --- |
    | ID | Integer | Primary Key |
    | Region | String | AWS region where the instance is located |
    | Instance Type | String | Type of EC2 instance |
    | State | String | Running or Stopped |
    | Launch Time | Datetime | Time when the instance was launched |
    | Termination Time | Datetime | Time when the instance was terminated |

    ## Traffic Data

    | Column Name | Data Type | Description |
    | --- | --- | --- |
    | Timestamp | Datetime | Timestamp of the traffic data |
    | Request Count | Integer | Number of requests at the timestamp |
    | Error Count | Integer | Number of errors at the timestamp |

    ## Predictions

    | Column Name | Data Type | Description |
    | --- | --- | --- |
    | Timestamp | Datetime | Timestamp of the prediction |
    | Instance Count | Integer | Number of instances to be launched at the prediction timestamp |


4. Cost-Optimized Scheduling:

    ## EC2 Instances

    | Column Name | Data Type | Description |
    | --- | --- | --- |
    | ID | Integer | Primary Key |
    | Region | String | AWS region where the instance is located |
    | Instance Type | String | Type of EC2 instance |
    | State | String | Running or Stopped |
    | Launch Time | Datetime | Time when the instance was launched |
    | Termination Time | Datetime | Time when the instance was terminated |

    ## EC2 Instance Types

    | Column Name | Data Type | Description |
    | --- | --- | ---
    | Name | String | Name of the EC2 instance type |
    | vCPU | Integer | Number of virtual CPUs |
    | Memory (GiB) | Float | Amount of memory in GiB |
    | Price per Hour | Float | Hourly price of the instance type |

    ## Cost Data

    | Column Name | Data Type | Description |
    | --- | --- | --- |
    | Timestamp | Datetime | Timestamp of the cost data |
    | Cost | Float | Total cost at the timestamp |

Other Features

## User Data

| Column Name | Data Type | Description |
| --- | --- | --- |
| ID | Integer | Primary Key |
| Name | String | Name of the user |
| Email | String | Email of the user |
| Role | String | Role of the user in the application (e.g. Admin, User) |

## Scheduling Configuration

| Column Name | Data Type | Description |
| --- | --- | --- |
| ID | Integer | Primary Key |
| User ID | Integer | Foreign Key referencing the User Data model |
| Schedule Name | String | Name of the scheduling configuration |
| Start Time | Datetime | Start time of the scheduling configuration |
| End Time | Datetime | End time of the scheduling configuration |
| Recurrence | String | Recurrence of the scheduling configuration (e.g. Daily, Weekly, Monthly) |
| Instance Type | String | EC2 instance type to be used in the scheduling configuration |

## Logs

| Column Name | Data Type | Description |
| --- | --- | --- |
| ID | Integer | Primary Key |
| Timestamp | Datetime | Timestamp of the log entry |
| User ID | Integer | Foreign Key referencing the User Data model |
| Action | String | Action performed by the user (e.g. Create, Update, Delete) |
| Description | String | Description of the action performed by the user |

## Notifications

| Column Name | Data Type | Description |
| --- | --- | --- |
| ID | Integer | Primary Key |
| Timestamp | Datetime | Timestamp of the notification |
| User ID | Integer | Foreign Key referencing the User Data model |
| Type | String | Type of the notification (e.g. Error, Info, Success) |
| Message | String | Message of the notification |



