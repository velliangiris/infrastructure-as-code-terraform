# infrastructure-as-code-terraform

In an overview, This is what we are doing in this configuration file.
 
 A Variable block where we define all the resource names that we are going to be using within the Terraform configuration
The second block is to tell Terraform to choose the right provider, in our case it is aws and we are also defining the region in this block on which our resources should be created
Creating a Security Group with inbound and outbound rules. We have two inbound rules and one outbound rule. we use lifecycle block to tell terraform to create the replacement resources first before destroying the live ones. this way we reduce downtime
Creating an EC2 instance, The instance type would be picked up from the variables block and we give some meaningful tags for management and future identification
nce the EC2 instance created, we would get the public IP of the instance. We are saving it as an output variable. The output variables would be saved locally and can be viewed anytime in the future with terraform output command
