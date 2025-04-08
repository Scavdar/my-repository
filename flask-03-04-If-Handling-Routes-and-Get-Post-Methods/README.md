# Hands-on Flask-03-04: If-For structure, Handling Routes and Get-Post Methods

Purpose of the this hands-on training is to give the students introductory knowledge of how to handle forms.

![HTTP Methods in Flask](./http-methods-flask.png)

## Learning Outcomes

At the end of the this hands-on training, students will be able to;

- build a simple web application with Flask framework.

- understand the HTTP request-response cycle and structure of URL.

- create routes (or views) with Flask.

- serve static content and files using Flask.

- serve dynamic content using the html templates.

- write html templates using Jinja Templating Engine.

- build a web application with Python Flask framework.

- create if conditions and for loops with flask.

- handle forms and GET-POST methods using the flask.

- use git repo to manage the application versioning.


## Outline

- Part 1 - Getting to know routing and HTTP URLs.

- Part 2 - Getting to know HTTP methods (GET & POST).

- Part 3 - Write a Web Application using If conditions and for loops

- Part 4 - Write a Web Application with Sample Routings and Templating on GitHub Repo

- Part 5 - Learn to use GET and POST HTTP Method

- Part 6 - Write a Sample Web Application with forms

## Part 1 - Getting to know routing and HTTP URLs.

HTTP (Hypertext Transfer Protocol) is a request-response protocol. A client on one side (web browser) asks or requests something from a server and the server on the other side sends a response to that client. When we open our browser and write down the URL (Uniform Resource Locator), we are requesting a resource from a server and the URL is the address of that resource. The structure of typical URL is as the following.

![URL anatomy](./url-structure.png)

The server responds to that request with an HTTP response message. Within the response, a status code element is a 3-digit integer defines the category of response as shown below.

- 1xx -> Informational ---> It means the request was received and the process is continuing.

- 2xx -> Success ---> It means the action was successfully received, understood, and accepted.

- 3xx -> Redirection ---> It means further action must be taken in order to complete the request.

- 4xx -> Client Error ---> It means the request contains incorrect syntax or cannot be fulfilled.

- 5xx -> Server Error ---> It means the server failed to fulfill an apparently valid request.

If you would learn those codes one by one. I can sent you a URL. You can also find different resources. 

https://www.w3schools.com/tags/ref_httpmessages.asp

## Part 2 - Getting to know HTTP methods (GET & POST)

HTTP (Hypertext Transfer Protocol) is a request-response protocol. A client on one side (web browser) asks or requests something from a server and the server on the other side sends a response to that client. 

When sending request, the client can send data with using different http methods like `GET, POST, PUT, HEAD, DELETE, PATCH, OPTIONS`, but the most common ones are `GET` and `POST`.

![Get and Post Requests](./get-post-request.jpg)

- HTTP `GET` method request;
    
    - used to request data from a specified resource.

    - can be cached.

    - remains in the browser history.

    - can be bookmarked

    - should never be used when dealing with sensitive data.

    - has length limitation.

    - only used to request data, not to modify it. 

- HTTP `POST` method request;
    
    - never cached.

    - does not remain in the browser history.

    - can not be bookmarked

    - can be used when dealing with sensitive data.

    - has no length limitation.

## Part 3 - Write a Web Application using If conditions and for loops

- Copy `flask-03-handling-routes-and-if-for` within `my-repository` repo

- Under `Flask_If_for_structure` folder within `flask-03-handling-routes-and-if-for` repo

- Create python file named `app.py`

```python
# Import Flask modules

# Create an object named app 

# Create a function named head which shows the massage as "This is my first conditions experience" in `index.html` 
# and assign to the route of ('/')

# Create a function named header which prints numbers elements of list one by one in `index.html` 
# and assign to the route of ('/')

# run this app in debug mode on your local.

```

## Part 4 - Write a Web Application with Sample Routings and Templating on GitHub Repo

- Let's head over `flask-03-handling-routes` folder within `flask-03-handling-routes-and-if-for` repo

- Create python file named `app.py`

```python
#Import Flask modules

#Create an object named app 


# Create a function named home which returns a string 'This is home page for no path, <h1> Welcome Home</h1>' 
# and assign route of no path ('/')


# Create a function named about which returns a formatted string '<h1>This is my about page </h1>' 
# and assign to the static route of ('about')


# Create a function named error which returns a formatted string '<h1>Either you encountered an error or you are not authorized.</h1>' 
# and assign to the static route of ('error')


# Create a function named admin which redirect the request to the error path 
# and assign to the route of ('/admin')


# Create a function named greet which return formatted inline html string 
# and assign to the dynamic route of ('/<name>')


# Create a function named greet_admin which redirect the request to the hello path with param of 'Master Admin!!!!' 
# and assign to the route of ('/greet-admin')


# Rewrite a function named greet which uses template file named `greet.html` under `templates` folder 
# and assign to the dynamic route of ('/<name>'). 
# Please find a template html file named `greet.html` which takes `name` as parameter under `templates` folder 


# Create a function named list10 which creates a list counting from 1 to 10 within `list10.html` 
# and assign to the route of ('/list10'). 
# Please find a template html file named `list10.html` which shows a list counting from 1 to 10 under `templates` folder 


# Create a function named evens which show the even numbers from 1 to 10 within `evens.html` 
# and assign to the route of ('/evens'). 
# Please find a template html file named `evens.html` which shows a list of even numbers from 1 to 10 under `templates` folder 


# Add a statement to run the Flask application which can be reached from any host on port 80.
```

## Part 5 - Learn to use GET and POST HTTP Method

- Go to `Flask_GET_POST_Methods` folder under the `flask-04-handling-forms-POST-GET-Methods` folder

- Create file named `app.py`  here. 

```python
# Import Flask modules


# Create an object named app


# create a function named "lcm" which calculates a least common multiple values of two numbers. 


# Create a function named `index` which uses template file named `index.html` 
# send two numbers as template variable to the app.py and assign route of no path ('/') 


# calculate sum of them using "lcm" function, then sent the result to the 
# "result.hmtl" file and assign route of path ('/calc'). 
# When the user comes directly "/calc" path, "Since this is a GET request, LCM has not been calculated" string returns to them with "result.html" file


# Add a statement to run the Flask application which can be debugged.

```

## Part 6 - Write a Sample Web Application with forms

- Go to `flask-04-handling-forms` within `flask-04-handling-forms-POST-GET-Methods` folder

- Now, we'll write an application with form handling and save the complete code as `app-form-handling.py` under `flask-04-handling-forms` folder.

```python
# Import Flask modules


# Create an object named app


# Write a function named `greet` which uses template file named `greet.html` given under 
# `templates` folder. it takes parameters from query string on URL, assign that parameter 
# to the 'user' variable and sent that user name into the html file. If it doesn't have any parameter, warning massage is raised


# Write a function named `greet` which uses template file named `greet.html` given under `templates` folder


# Write a function named `login` which uses `GET` and `POST` methods, 
# and template files named `login.html` and `secure.html` given under `templates` folder 
# and assign to the static route of ('login')


# Add a statement to run the Flask application which can be reached from any host on port 80.


# app.run(host='0.0.0.0', port=80)
```

\\\\\\\\\\\\\\\//////////////\\\\\\\\\\\\\/////////////\\\\\\\\\\\\\//////////\\\\\\\\\\\\\\\\\\\\\\\//////////////\\\\\\\//////


1# AWSTemplateFormatVersion: 2010-09-09

Description: |
  Template to build the phonebook app and infrastructure

Parameters:

  vpc:
    Description: VPC ID
    Type: AWS::EC2::VPC::Id

  
Resources:

  sgRds:
    Type: AWS::EC2::SecurityGroup
    Properties:
      GroupDescription: "Allow access to RDS"
      GroupName: "RDSAccess"
      SecurityGroupIngress: 
        - IpProtocol: tcp
          FromPort: 3306
          ToPort: 3306
          CidrIp: "0.0.0.0/0"
      VpcId: !Ref vpc

  rdsDatabase:
    Type: AWS::RDS::DBInstance
    Properties:
      Engine: mysql
      EngineVersion: "8.0.39"
      Port: "3306"
      DBInstanceIdentifier: phonebook-instance
      DBName: clarusway_phonebook
      MasterUsername: admin
      MasterUserPassword: clarusway_1234
      DBInstanceClass: db.t2.micro
      AllocatedStorage: "20"
      MultiAZ: false
      VPCSecurityGroups: 
        - !Ref sgRds
      AllowMajorVersionUpgrade: false
      AutoMinorVersionUpgrade: false
      DeletionProtection: false
      PubliclyAccessible: false
      BackupRetentionPeriod: 0
      
      MasterUsername: admin
      MasterUserPassword: clarusway_1234

      ParameterName:
    Description: 
    Type: AWS::EC2::VPC::Id
    Default: 

    AWSTemplateFormatVersion: 2010-09-09

Description: |
  Template to build the phonebook app and infrastructure

Parameters:

  vpc:
    Description: VPC ID
    Type: AWS::EC2::VPC::Id

  
Resources:

  sgRds:
    Type: AWS::EC2::SecurityGroup
    Properties:
      GroupDescription: "Allow access to RDS"
      GroupName: "RDSAccess"
      SecurityGroupIngress: 
        - IpProtocol: tcp
          FromPort: 3306
          ToPort: 3306
          CidrIp: "0.0.0.0/0"
      VpcId: !Ref vpc

  rdsDatabase:
    Type: AWS::RDS::DBInstance
    Properties:
      Engine: mysql
      EngineVersion: "8.0.39"
      Port: "3306"
      DBInstanceIdentifier: phonebook-instance
      DBName: clarusway_phonebook
      MasterUsername: admin
      MasterUserPassword: clarusway_1234
      DBInstanceClass: db.t2.micro
      AllocatedStorage: "20"
      MultiAZ: false
      VPCSecurityGroups: 
        - !Ref sgRds
      AllowMajorVersionUpgrade: false
      AutoMinorVersionUpgrade: false
      DeletionProtection: false
      PubliclyAccessible: false
      BackupRetentionPeriod: 0

      EngineVersion: "8.0.39"
      DBInstanceClass: db.t3.micro

       PubliclyAccessible: true
      BackupRetentionPeriod: 0
      ApplyImmediately: true

      #db_endpoint = open("/home/ec2-user/dbserver.endpoint", 'r', encoding='UTF-8').readline().strip()
db_endpoint = "phonebook-instance.cbanmzptkrzf.us-east-1.rds.amazonaws.com"

# Configure mysql database

app.config['MYSQL_DATABASE_HOST'] = db_endpoint
DEVELOPER_NAME="Altaz"

# This "/home/ec2-user/dbserver.endpoint" file has to be created from cloudformation template and it has RDS endpoint
db_endpoint_file = open("/home/ec2-user/dbserver.endpoint", 'r', encoding='UTF-8')
db_endpoint = db_endpoint_file.readline().strip()
#db_endpoint = "phonebook-instance.cbanmzptkrzf.us-east-1.rds.amazonaws.com"
db_endpoint_file.close()

git add .
git commit -m "add phonebook"
git push

if __name__== '__main__':
    init_phonebook_db()
    # app.run(debug=True)
    app.run(host='0.0.0.0', port=80) 

    git add .
git commit -m "update port and host"
git push

#! /bin/bash -x
yum update -y
yum install python3 -y
yum install python3-pip -y
pip3 install flask
pip3 install flask_mysql
echo "${MyDBURI}" > /home/ec2-user/dbserver.endpoint
FOLDER="https://raw.githubusercontent.com/altazbhanji/my-repository/refs/heads/main/Project-004-Phonebook-Application/"
curl -s --create-dirs -o "/home/ec2-user/templates/index.html" -L "$FOLDER"templates/index.html
curl -s --create-dirs -o "/home/ec2-user/templates/add-update.html" -L "$FOLDER"templates/add-update.html
curl -s --create-dirs -o "/home/ec2-user/templates/delete.html" -L "$FOLDER"templates/delete.html
curl -s --create-dirs -o "/home/ec2-user/phonebook-app.py" -L "$FOLDER"phonebook-app.py
python3 /home/ec2-user/phonebook-app.py


 LogicalID:
    Type: AWS::ElasticLoadBalancingV2::TargetGroup
    Properties:
      Port: "Number"
      Protocol: "String"
      VpcId: "String"  
      TargetType: "String"
      HealthyThresholdCount: "Number"
      UnhealthyThresholdCount: "Number"
9:20
  elbTargetGroup:
    Type: AWS::ElasticLoadBalancingV2::TargetGroup
    Properties:
      Port: 80
      Protocol: HTTP
      VpcId: !Ref vpc 
      TargetType: instance
      HealthyThresholdCount: 2
      UnhealthyThresholdCount: 2
9:21
  LogicalID:
    Type: AWS::EC2::SecurityGroup
    Properties:
      GroupDescription: "String" # Required
      GroupName: "String"
      SecurityGroupIngress: 
        - IpProtocol: "String"
          FromPort: "Number"
          ToPort: "Number"
          CidrIp: "String"
      VpcId: "String"
9:23
  sgElb:
    Type: AWS::EC2::SecurityGroup
    Properties:
      GroupDescription: "Allow HTTP from Internet"
      GroupName: HttpFromAnywhere
      SecurityGroupIngress: 
        - IpProtocol: tcp
          FromPort: 80
          ToPort: 80
          CidrIp: "0.0.0.0/0"
      VpcId: !Ref vpc
9:26
  LogicalID:
    Type: AWS::ElasticLoadBalancingV2::Listener
    Properties:
      DefaultActions: # Required
        - TargetGroupArn: "String"
          Type: "String"
      LoadBalancerArn: "String" # Required
      Port: "Number"
      Protocol: "String"
9:29
  elbListener:
    Type: AWS::ElasticLoadBalancingV2::Listener
    Properties:
      DefaultActions: 
        - TargetGroupArn: !Ref elbTargetGroup
          Type: forward
      LoadBalancerArn: "String"
      Port: 80
      Protocol: HTTP
9:34
  ParameterName:
    Description: 
    Type: List<AWS::EC2::Subnet::Id>
    Default:     
9:37
  elbLoadBalancer:
    Type: AWS::ElasticLoadBalancingV2::LoadBalancer
    Properties:
      Name: phonebook-loadbalancer
      Type: application
      Scheme: internet-facing
      IpAddressType: ipv4
      SecurityGroups: 
        - !Ref sgElb
      Subnets: !Ref subnets


  elbListener:
    Type: AWS::ElasticLoadBalancingV2::Listener
    Properties:
      DefaultActions:
        - TargetGroupArn: !Ref elbTargetGroup
          Type: forward
      LoadBalancerArn: !Ref elbLoadBalancer
      Port: 80
      Protocol: HTTP
9:41
Parameters:

  vpc:
    Description: VPC ID
    Type: AWS::EC2::VPC::Id

  subnets:
    Description: Subnets for load balancer
    Type: List<AWS::EC2::Subnet::Id>

  


Altaz - Instructor
  9:55 PM
echo "${MyDBURI}" > /home/ec2-user/dbserver.endpoint
9:59
  ec2LaunchTemplate:
    Type: AWS::EC2::LaunchTemplate
    Properties:
      LaunchTemplateData:
        ImageId: "{{resolve:ssm:/aws/service/ami-amazon-linux-latest/al2023-ami-kernel-6.1-x86_64}}"
        InstanceType: t2.micro
        KeyName: !Ref keypairname
        SecurityGroupIds:
          - !Ref sgElb
        TagSpecifications:
          - ResourceType: instance
            Tags:
              - Key: Name
                Value: phonebook-server
        UserData:
          Fn::Base64:
            !Sub
              - |
                #! /bin/bash -x
                yum update -y
                yum install python3 -y
                yum install python3-pip -y
                pip3 install flask
                pip3 install flask_mysql
                echo "${MyDBURI}" > /home/ec2-user/dbserver.endpoint
                FOLDER="https://raw.githubusercontent.com/altazbhanji/my-repository/refs/heads/main/Project-004-Phonebook-Application/"
                curl -s --create-dirs -o "/home/ec2-user/templates/index.html" -L "$FOLDER"templates/index.html
                curl -s --create-dirs -o "/home/ec2-user/templates/add-update.html" -L "$FOLDER"templates/add-update.html
                curl -s --create-dirs -o "/home/ec2-user/templates/delete.html" -L "$FOLDER"templates/delete.html
                curl -s --create-dirs -o "/home/ec2-user/phonebook-app.py" -L "$FOLDER"phonebook-app.py
                python3 /home/ec2-user/phonebook-app.py
              - MyDBURI: !GetAtt rdsDatabase.Endpoint.Address
9:59
  keypairname:
    Description: Key Pair Name
    Type: AWS::EC2::KeyPair::KeyName


Altaz - Instructor
  10:05 PM
  asgAutoScalingGroup:
    Type: AWS::AutoScaling::AutoScalingGroup
    Properties:
      AvailabilityZones: !GetAZs ""
      DesiredCapacity: "2"
      HealthCheckGracePeriod: 180
      HealthCheckType: ELB
      LaunchTemplate:
        LaunchTemplateId: !Ref ec2LaunchTemplate
        Version: !GetAtt ec2LaunchTemplate.LatestVersionNumber
      MaxSize: "3"
      MinSize: "1"
      TargetGroupARNs: 
        - !Ref elbTargetGroup
10:09
  ec2LaunchTemplate:
    Type: AWS::EC2::LaunchTemplate
    Properties:
      LaunchTemplateData:
        ImageId: "{{resolve:ssm:/aws/service/ami-amazon-linux-latest/al2023-ami-kernel-6.1-x86_64}}"
        InstanceType: t2.micro
        KeyName: !Ref keypairname
        SecurityGroupIds:
          - !Ref sgElb
        TagSpecifications:
          - ResourceType: instance
            Tags:
              - Key: Name
                Value: phonebook-server
        UserData:
          Fn::Base64:
            !Sub
              - |
                #! /bin/bash -x
                yum update -y
                yum install python3 -y
                yum install python3-pip -y
                pip3 install flask
                pip3 install flask_mysql
                echo "${MyDBURI}" > /home/ec2-user/dbserver.endpoint
                FOLDER="https://raw.githubusercontent.com/altazbhanji/my-repository/refs/heads/main/Project-004-Phonebook-Application/"
                curl -s --create-dirs -o "/home/ec2-user/templates/index.html" -L "$FOLDER"templates/index.html
                curl -s --create-dirs -o "/home/ec2-user/templates/add-update.html" -L "$FOLDER"templates/add-update.html
                curl -s --create-dirs -o "/home/ec2-user/templates/delete.html" -L "$FOLDER"templates/delete.html
                curl -s --create-dirs -o "/home/ec2-user/phonebook-app.py" -L "$FOLDER"phonebook-app.py
                python3 /home/ec2-user/phonebook-app.py
              - MyDBURI: !GetAtt rdsDatabase.Endpoint.Address
10:13
AWSTemplateFormatVersion: 2010-09-09

Description: |
  Template to build the phonebook app and infrastructure

Parameters:

  vpc:
    Description: VPC ID
    Type: AWS::EC2::VPC::Id

  subnets:
    Description: Subnets for load balancer
    Type: List<AWS::EC2::Subnet::Id>

  keypairname:
    Description: Key Pair Name
    Type: AWS::EC2::KeyPair::KeyName

  
Resources:

  asgAutoScalingGroup:
    Type: AWS::AutoScaling::AutoScalingGroup
    Properties:
      AvailabilityZones: !GetAZs ""
      DesiredCapacity: "2"
      HealthCheckGracePeriod: 180
      HealthCheckType: ELB
      LaunchTemplate:
        LaunchTemplateId: !Ref ec2LaunchTemplate
        Version: !GetAtt ec2LaunchTemplate.LatestVersionNumber
      MaxSize: "3"
      MinSize: "1"
      TargetGroupARNs: 
        - !Ref elbTargetGroup

  ec2LaunchTemplate:
    Type: AWS::EC2::LaunchTemplate
    Properties:
      LaunchTemplateData:
        ImageId: "{{resolve:ssm:/aws/service/ami-amazon-linux-latest/al2023-ami-kernel-6.1-x86_64}}"
        InstanceType: t2.micro
        KeyName: !Ref keypairname
        SecurityGroupIds:
          - !Ref sgElb
        TagSpecifications:
          - ResourceType: instance
            Tags:
              - Key: Name
                Value: phonebook-server
        UserData:
          Fn::Base64:
            !Sub
              - |
                #! /bin/bash -x
                yum update -y
                yum install python3 -y
                yum install python3-pip -y
                pip3 install flask
                pip3 install flask_mysql
                echo "${MyDBURI}" > /home/ec2-user/dbserver.endpoint
                FOLDER="https://raw.githubusercontent.com/altazbhanji/my-repository/refs/heads/main/Project-004-Phonebook-Application/"
                curl -s --create-dirs -o "/home/ec2-user/templates/index.html" -L "$FOLDER"templates/index.html
                curl -s --create-dirs -o "/home/ec2-user/templates/add-update.html" -L "$FOLDER"templates/add-update.html
                curl -s --create-dirs -o "/home/ec2-user/templates/delete.html" -L "$FOLDER"templates/delete.html
                curl -s --create-dirs -o "/home/ec2-user/phonebook-app.py" -L "$FOLDER"phonebook-app.py
                python3 /home/ec2-user/phonebook-app.py
              - MyDBURI: !GetAtt rdsDatabase.Endpoint.Address
                        
                        
  elbLoadBalancer:
    Type: AWS::ElasticLoadBalancingV2::LoadBalancer
    Properties:
      Name: phonebook-loadbalancer
      Type: application
      Scheme: internet-facing
      IpAddressType: ipv4
      SecurityGroups: 
        - !Ref sgElb
      Subnets: !Ref subnets


  elbListener:
    Type: AWS::ElasticLoadBalancingV2::Listener
    Properties:
      DefaultActions:
        - TargetGroupArn: !Ref elbTargetGroup
          Type: forward
      LoadBalancerArn: !Ref elbLoadBalancer
      Port: 80
      Protocol: HTTP

  sgElb:
    Type: AWS::EC2::SecurityGroup
    Properties:
      GroupDescription: "Allow HTTP from Internet"
      GroupName: HttpFromAnywhere
      SecurityGroupIngress: 
        - IpProtocol: tcp
          FromPort: 80
          ToPort: 80
          CidrIp: "0.0.0.0/0"
      VpcId: !Ref vpc

  elbTargetGroup:
    Type: AWS::ElasticLoadBalancingV2::TargetGroup
    Properties:
      Port: 80
      Protocol: HTTP
      VpcId: !Ref vpc 
      TargetType: instance
      HealthyThresholdCount: 2
      UnhealthyThresholdCount: 2

  sgRds:
    Type: AWS::EC2::SecurityGroup
    Properties:
      GroupDescription: "Allow access to RDS"
      GroupName: "RDSAccess"
      SecurityGroupIngress: 
        - IpProtocol: tcp
          FromPort: 3306
          ToPort: 3306
          CidrIp: "0.0.0.0/0"
      VpcId: !Ref vpc

  rdsDatabase:
    Type: AWS::RDS::DBInstance
    Properties:
      Engine: mysql
      EngineVersion: "8.0.39"
      Port: "3306"
      DBInstanceIdentifier: phonebook-instance
      DBName: clarusway_phonebook
      MasterUsername: admin
      MasterUserPassword: clarusway_1234
      DBInstanceClass: db.t3.micro
      AllocatedStorage: "20"
      MultiAZ: false
      VPCSecurityGroups: 
        - !Ref sgRds
      AllowMajorVersionUpgrade: false
      AutoMinorVersionUpgrade: false
      DeletionProtection: false
      PubliclyAccessible: true
      BackupRetentionPeriod: 0
      ApplyImmediately: true


#Outputs: