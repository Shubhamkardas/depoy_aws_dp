
# Deploying a Node Js Application on AWS EC2

### Set up an AWS EC2 instance

1. Create an IAM user & login to your AWS Console
    - Access Type - Password
    - Permissions - Admin
2. Create an EC2 instance
    - Select an OS image - Ubuntu
    - Create a new key pair & download `.pem` file
    - Instance type - t2.micro
3. Connecting to the instance

1. Clone this project
```
git clone https://github.com/Shubhamkardas/depoy_aws_dp.git
```
2. create  - `(.env)` file
touch .env
copy public key and secret key from stripe
```
DOMAIN= ""
PORT=3000
STATIC_DIR="./client"

PUBLISHABLE_KEY=""
SECRET_KEY=""
```
3. Updating the outdated packages and dependencies
```
sudo apt update
sudo apt install nodejs
sudo apt install npm
```
4. Initialise and start the project
```
npm install
npm run start
```
> NOTE - We will have to edit the **inbound rules** in the security group of our EC2, in order to allow traffic from our particular port

### Project is deployed on AWS 🎉
=======
