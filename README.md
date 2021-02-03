# Cloud_1
## Project description:
##### This is 42 programme's introduction to cloud services project.
##### In this project, students have to build a simple cloud infrastructure that must be able to:
    . Host a simple wordpress website.
    . Have a minimum of two server instances running at the same time at all times.
    . Randomly and evenly redirect visitors to any of the running servers.
    . In case of traffic piking, more server instances should be  automatically launched to accomodate this.
    . When traffic subsides, the server instances should revert back to two server instances.
    . A CDN should be used to distribute the static content.
    . New content should be available within a few seconds of uploading across all instances.
    . Your website should continue to be available despite any failures that might occur.
    . You should make sure that the public only has access to the stuff they are allowed to.

## How I handled the project:
    . I created an account with AWS (https://docs.aws.amazon.com/).
    . After following the registration process and my account was approved,
    . I logged into my account on AWS Console and subscribed to Elastic Beanstalk service for web environment.
    . In Elastic Beanstalk I selected web server environment on the environment tier options.
    . After selecting environment tier, I gave my application and environment their names.
    . In the platform option I chose AWS managed platform of PHP, and went with sample application in application code.
    . then created environment (this might take a bit).
    . I subscribed to the ec2 services to establish the instances.
    . In the capacity configuration, I chose the load balanced environment type.
    . This will allow us to have multiple instances running.
    . in the security configuration, I set the inbound rules to:
        . http:80:anywhere.
        . https:443:anywhere.
        . ssh:22:only my ip.
    . I subscribed to the S3 bucket to contain my images and stuff like that.
    . 