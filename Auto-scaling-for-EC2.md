# To configure Auto scaling we need to setup various AWS services before that.
  # Launch template consist of
    AMI and Instance type
    EBS volume
    Security groups
    user interface profile
    user data
    key pairs
    termination protection
    etc....

# Now Auto-scaling group consist of
  VPC subnets
  ELB (optional)
  health checks EC2/ELB
  group size & policy

# remember Auto-scaling will use Cloudwatch in the background to monitor whether or not it needs to scale out or scale back in, 
  and also if any of the instance fails to respond to health checks auto-scaling will terminate that instance and replace with fresh, healthy instance.
