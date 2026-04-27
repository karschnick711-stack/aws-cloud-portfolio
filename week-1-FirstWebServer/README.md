# Week 1 - Launching EC2 Instance and Starting Web Server in Linux

## Objective

Build web environment in AWS using:

* EC2
* Security Groups

---

## Architecture

Internet → EC2 Instances

---

## Skills Practiced

* Launching EC2 instances
* Configuring security groups
* Installing Apache

---

## Security Design

The EC2 instances allowed HTTP traffic from the the public internet.

---

## Problems Encountered

### NA

Verified:

* Instance running?
* Apache (httpd) running?
* Security group allowing traffic? port 80 inbound rule from anywhere? 0.0.0.0/0?

---  

## Commands used

sudo dnf update -y
sudo dnf install -y httpd
sudo systemctl start httpd
sudo systemctl enable httpd
-used to download and install apache to the server, start the server and enable the service so starts automatically on reboot

echo "Kevin Day 1 Cloud Lab" | sudo tee /var/www/html/index.html
-creating/naming the website

curl localhost
-testing the website locally
-outcome- saw "Kevin Day 1 Cloud Lab"

---

## What I Learned

1. How to start an EC2 instance
2. How to download/install apache to linux server
3. How to test the service locally
4. How to troubleshoot if the website doesn't load.
   *Is the instance running in EC2?
   *Is the web service running - sudo systemctl status httpd (running?)
   *Is the security group allowing traffic? - port 80 inbound rule http from anywhere 0.0.0.0/0

---

## Future Improvements

*Learn to launch an instance with user data
*Learn to attach volumes to instances
*Learn how to build servers from snapshots
*Learn how to build target groups and automatic scaling groups
