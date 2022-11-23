# Website-Monitoring-using-AWS-Lambda-and-Aurora
Website Monitoring service checks and verifies the website is up and working as expected and website visitors can use the site without facing any difficulties as expected

## Architecture
![image](https://user-images.githubusercontent.com/103509243/203448838-df2471d0-652f-4e55-be15-58700519540c.png)

## Approach  
(1) Launch an EC2 instance on AWS and install Amazon Kinesis    
(2) Create a Data analytics streams in amazon Kinesis for real-time streaming of data  
(3) Create another Kinesis streams to control the amount of messages being delivered in case of spike cause downtime  
(4) If receive excessive messages, then trigger Lambda  
(5) Lambda triggers SNS notification which in turn delivers SMS message. Also, the error messages will be saved in Aurora RDBMS for future analysing
