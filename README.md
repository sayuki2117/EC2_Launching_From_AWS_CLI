# =Creating/Launch an EC2 instance on AWS CLI Process=
To be able to launch an EC2 Instance in AWS CLI, one have to download, install and configure the AWS CLI application on his computer.

## Download, Install, and Configuration of AWS-CLI on my Computer
### 1. The AWS CLI downloaded from the AWS website.

#### 2. Install the AWS CLI.
   After Download Double-click the AWS CLI installer to start the installation process. Follow the on-screen instructions to complete the installation.
   ![AWS Config](<aws cli config.PNG>)
   ![AWS Config](<1 aws cli config.PNG>)


### 3. Configure the AWS CLI.
   To configure the AWS CLI, you need to set your AWS access key ID and secret access key. You can find your AWS access key ID and secret access key in the AWS Console.
   to be sure of your configuration use the following commands
   ![AWS Config](<aws cli config.PNG>)
$ aws configure list
      Name                    Value             Type    Location
      ----                    -----             ----    --------
   profile                <not set>             None    None
access_key     ****************AB5G shared-credentials-file
secret_key     ****************2DHC shared-credentials-file
    region                us-west-2      config-file    ~/.aws/config

## Security Group Creation Steps:
    The aws ec2 create-security-group command to create a security group, which is a firewall that controls the traffic that can flow to and from your EC2 instance.
    The command used:  aws ec2 create-security-group --group-name wizy-sg --description "this my security group" --vpc-id vpc-0450fd5913e0189b1
![AWS SG](<Security Group.PNG>)

## Creation/Launch of instance From Cli:
The following command was used: aws ec2 run-instances --image-id ami-04288abc8d2000768 --count 1 --instance-type t2.micro --key-name instance-key-pair --security-groups wizy-sg
 ![Alt text](<instance launch.PNG>) 
 ![Alt text](<instance launch1.PNG>)
### View Instance Running from AWS Management console:
 ![Alt text](<instance launch on console.PNG>)
### View Instance Running from AWS CLI:
 ![Alt text](<instance running.PNG>)
### Instance Termination from AWS CLI using this command:
aws ec2 terminate-instances --instance-ids i-0e567b637e8c4e710
![Alt text](<instance termination.PNG>)
![Alt text](<instance termination1.PNG>)
### Instance keypair deletion using the following command:
aws ec2 delete-key-pair --key-name instance-key-pair 
![Alt text](<delete keypair and SG.PNG>)

# ...The Process for Creating/Launching and Terminating an EC2 Instance using the AWS-CLI was successfully done...

  


