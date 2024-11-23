# Steps to setup Load Balancer-
  1) create a VPC
  2) we need to work in two availability zones - One & Two
  3) each availability zone comprises of one public subnet A & B respectively.
  4) we need setup two security groups, one which allows inbound traffic on port 80 and port 22, other security group will be allocated to the ELB.
  5) then we will deploy two EC2 Instances using a standard linux two ami and a script (download from source udemy course),
     with the help of ami and script, we will provision two servers webserver-1 one and webserver-2 in availability zone-one and availability zone-two respectively.
  6) now setup the target group, it will have the health monitoring system that will monitor the EC2 instance we registr against the target group.
  7) now we will place Application Load Balancer configured to forward traffic to that target group.
  8) when we deploy the Application Load Balancer we need to specify the availability zone and specifically the subnets
