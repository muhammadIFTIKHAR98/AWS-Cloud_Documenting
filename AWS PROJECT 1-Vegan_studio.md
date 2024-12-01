# VEGAN STUDIO RECIPE CONTEST
  -> CONTEXT (CASE STUDY)
  
    1) The vacant studio comprises of a chain of coffee shops and restaurants across the UK, and it serves its patrons with a wide range of 
        healthy vegan dishes. Served throughout the day for breakfast, lunch and dinner.

    2) The vacant studio advocates plant based diet as a way to achieve healthy living lifestyles.Now, as part of a well thought out marketing 
        strategy, the vacant studio has come up with several different ideas in order to build brand awareness and encourage more sales.

    3) In this project, we're going to take a look at a typical use case proposed by the marketing department in order to help the vacant 
        studio increase its customer base. So the marketing department has come up with the most brilliant idea of launching a recipe contest 
        where members of the public will be invited to submit their favorite vacant recipes by creating a recipe contest that's open to members 
        of the public.
   
    4) The vacant studio hopes to increase brand awareness, increase more sales and win over the competition.

    5) Let's take a look at the specifics of the vacant studio's requirement.
       - So Sarah, our marketing head, has convinced the board of directors at the vacant studio to launch a web page on its corporate website, 
         which would enable members of the public to enter a favorite vacant recipe contest.
       - Members of the public will be allowed to submit one recipe of their favorite vacant dish.
       - And Becky, our head chef, along with her team, will review all submitted recipes and pick one recipe which will be prepared by the team.
       - The criteria for choosing the winning recipe will be based on several factors, including choice of ingredients, unique style of 
         preparation and cooking method, and most importantly, taste.
       - The winner's recipe will then be published on the Vacant Studios blog site, and the dish will be named after the winner and served across 
         all cafes and restaurants.The winner will also receive a cash reward of $1,000.

    6) Let's take a look at the key benefits that the vegan studio hopes to achieve by implementing such a solution.
       - So one of the key benefits here is that the vegan studio will help build a community when a contest is run effectively, it is a great way 
         to build a strong following. It will incentivize people to follow the vegan studios blog site, Social Media,ET Cetera.
       - It will build brand awareness and that brand awareness will help win over the competition.It will increase subscribers because if you're 
         giving a free giveaway, as in the case of a contest, then obviously you're going to encourage more people to sign up.
       - It will increase sales because hopefully the brand awareness will encourage members of the public to visit our cafes and restaurants and 
         it will obviously increase customer engagement.

  -> SOLUTION 

    1) First of all we need to create an architectural Design to understand and get a clear picture of which AWS services will be required and how 
        they will be interconnected.
    2) select the region (here we will select the london region).
    3) create a VPC (named as  vs-vpc).
    4) now create 6 subnets within the VPC within 2 availability zone.
        - 2 public subnet named vpc-public-subnet-1 and 2 in availability zone 1 and 2 respectively.
        - 4 private subnet named vpc-app-subnet-1 and 2, vpc-data-subnet-1 and 2 in availability zone 1 and 2 respectively.
    5) Setup the Internet gateway
    6) Setup the NAT gateway in any public subnet, this will be used to help the private subnets services like EC2 to access the internet as the 
        private subnets doesn't have internet acces and public IP address.
    7) 
