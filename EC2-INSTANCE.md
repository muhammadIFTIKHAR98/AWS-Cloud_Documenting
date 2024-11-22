# TO create EC2 Instance in AWS there are several steps to keep in mind
  1) selct the region
  2) name your instance
  3) select AMI(amazon machine image)
           - An AMI is a template that contains the software configuration (operating system, application server, and applications) required to launch your instance.
             Search or Browse for AMIs if you don’t see what you are looking for below.
  4) select instance type (t2.micro is selected by me)
  5) create new key pair
           - You can use a key pair to securely connect to your instance. Ensure that you have access to the selected key pair before you launch the instance.
             this key pair will be used further to generate the id and password to login into Ami server (usually windows server).
  6) create security group.
  7) configure storage
  8) now in advanced details kindly select following options,
            shut down behavior-stop
            termination protection- Enable
            stop protection- Enable
            select purchasing option- none / spot instance
            tenancy- shared

  9) Launch the instance
           
