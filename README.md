## Application Overview
![multi_containers_aws drawio](https://user-images.githubusercontent.com/114280300/221367356-369b2e6f-8aab-4e65-b6d8-2b322530c56b.png)




## Deployment workflow

![multi_containers_deployment drawio](https://user-images.githubusercontent.com/114280300/221367114-a37ae6a4-d210-4555-8bbe-cfd88579a59c.png)

## AWS VPC's and Security Groups
- When create aws instances/services, it was created in a specific region of the world (Amazon has a variety of regions / data centers).
- In each of these different regions, we will have a VPC (Virtual Private Cloud) created by default (We can have multiple VPC's in one region). 
- A VPC is essentially kinda like a own private network so that every instance/service that we create is isolated to just our account. For instance, when we created elastic beanstalk instance, only our account can access to that instance
- AWS services by default can not talk to each other. To get these different services to connect to each other , we have to create a security group(firewall rules) and apply it our instances/services:
![vpc_security_groups drawio](https://user-images.githubusercontent.com/114280300/221369112-7ceb292b-ea51-460e-bf0b-223c147b8c87.png)
- By default when create EB instance, a security group was created and apply to the EB instance (this security group will allow any incoming traffic on port 80 from any IP)
