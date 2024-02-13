# AWS-Cloud-Projects  - Cloud computing with AWS -heading 1

# Setting up a VPC and its Components

![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC.png)

## Introduction -sub heading
A Virtual Private Cloud (VPC) is a cloud computing infrastructure that closely resembles a traditional physical datacenter in its functionality. Serving as the networking backbone of the cloud, a VPC seamlessly connects various components and facilitates efficient communication within the cloud environment. This expansive network extends across a designated **region**, providing a scalable and secure framework for hosting and managing resources in the cloud. Some key components of a Virtual Private Cloud (VPC) include but not limited to subnets, security groups, and route tables.

## **Step by step guide**

I will guide you through a comprehensive, step-by-step process for setting up a Virtual Private Cloud (VPC) using the management console. Upon launching the console, here's what you can anticipate. Keep in mind that the interface may vary if you have previously engaged with different services.

![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC%20aws/Management%20console%20home%20page.png)



## Step 1 : Creating the VPC

Navigate to the top search bar and enter "VPC" to initiate the process. This action will lead you to the relevant section within the management console where you can configure and manage your Virtual Private Cloud settings.

![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC%20aws/Search%20VPC.png)


Choose the "VPC" option from the search results to be directed to the VPC dashboard. This dashboard is the central hub for configuring and overseeing your Virtual Private Cloud settings, allowing you to efficiently manage and customize your cloud networking infrastructure.

![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC%20aws/Create%20vpc%20dashboard.png)


Click on the "Create VPC" option located at the top, adjacent to the "Launch EC2 Instances." This action will take you to the setup interface where you can begin configuring your new VPC. The screen will present you with a series of fields and options to define the parameters of your Virtual Private Cloud. 

This is what you should see
![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC%20aws/Create%20vpc%20page.png)


Opting for the "VPC Only" option indicates your intention to have precise control over the components associated with the VPC. Proceed by filling in the parameters according to the specific requirements of your project. Input the necessary details such as the VPC name, IPv4 CIDR block, and any additional settings that align with your project's networking needs. Ensure that the configurations are in line with your project's specifications for a tailored and optimized Virtual Private Cloud.

![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC%20aws/VPC%20name%20and%20CIDR.png)

CIDR, which stands for Classless Inter-Domain Routing, is a method for specifying IP addresses and their associated routing behavior. It allows for more flexible allocation of IP addresses than the traditional class-based addressing.

When setting up a Virtual Private Cloud (VPC) and defining its CIDR block, you need to choose a range of IP addresses that will be used within the network. The CIDR block is specified in the form of a range, such as 10.0.0.0/16, where the "10.0.0.0" represents the network address, and the "/16" indicates the subnet mask.

For example, in 10.0.0.0/16:

    "10.0.0.0" is the network address.
    "/16" represents the subnet mask, indicating that the first 16 bits are used for the network portion, leaving 32 - 16 = 16 bits for host addresses.

Choosing an appropriate CIDR block depends on the number of hosts you expect to have in your network and the level of granularity you need for subnetting. A larger CIDR block provides more IP addresses but may result in larger broadcast domains, while a smaller CIDR block offers fewer addresses but allows for more efficient use of address space.

Ensure that the CIDR block you choose doesn't overlap with any existing networks, either within your cloud environment or externally. Additionally, consider future scalability requirements when selecting the CIDR block for your VPC.

After filling in all the necessary parameters for your VPC, proceed to the bottom of the page and select the "Create VPC" option. This action will initiate the creation process, and your Virtual Private Cloud will be provisioned with the specified configurations. 

![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC%20aws/Create%20VPC.png)

Congratulations! You've successfully created a VPC. 

![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC%20aws/Successfully%20created%20VPC.png)

It's crucial to be aware that alongside the VPC you've created, there may be default VPCs present in your cloud environment. These default VPCs are automatically generated by the cloud provider and can serve as a quick-start option for users who want a pre-configured networking environment.

While my custom VPC, named "Zakayo," reflects my specific configurations and preferences, the default VPCs often come with predefined settings for ease of use. Be mindful of both your custom VPC and any default VPCs present, ensuring that your resources are appropriately organized and configured within the desired network structure.

![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC%20aws/My%20VPCs.png)


It's important to note that while the VPC infrastructure is in place, its full potential comes to life when you start populating it with resources. Whether it's deploying instances, setting up databases, or configuring other services, the real power of your VPC unfolds as you add and manage resources within this cloud networking environment.

## Step 2 : Creating subnets

Subnets are a way of dividing a larger network, into smaller and more manageable segments. This segmentation provides several benefits, including improved network organization, enhanced security, and more efficient resource management. Subnets are designed to span across availability zones within a chosen region. This approach enhances reliability and fault tolerance by strategically distributing network resources.

To create a subnet, go to the VPC dashboard on the left side of the management console, and select "Subnets." This will lead you to the Subnets section, where you can create and manage subnets within your Virtual Private Cloud (VPC).

![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC%20aws/No%20Subnets.png)

While default subnets are often automatically generated, creating your own subnets based on your specific needs is advisable. This customization allows you to fine-tune the network structure to meet your requirements, ensuring a more tailored approach to resource allocation, security, and overall management within your cloud environment. Select the "Create Subnet" option located at the top right of the Subnets section to initiate the process of customizing and adding a new subnet to your Virtual Private Cloud (VPC).

![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC%20aws/Create%20Subnets.png)

Customize the subnet settings by filling in the required details. This involves specifying parameters such as the VPC association, choosing the availability zone, and defining the CIDR block for the subnet. Ensure that the settings align with your project's networking needs and provide the necessary segmentation within your Virtual Private Cloud (VPC). 

![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC%20aws/Select%20VPC%20to%20associate%20with%20subnet.png)


![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC%20aws/edit%20subnet%20settings.png)

Once all the parameters are configured to your specifications, navigate to the bottom of the page and click on the "Create Subnets" option.

Upon revisiting the Subnets section, you will observe that the newly configured subnets have been successfully added. Congratulations for coming this far!

![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC%20aws/Created%20Subnets.png)

In my case, I've created two subnets named "Zakayo_calmDown1" and "Zakayo_calmDown2," both associated with the "Zakayo" VPC. The "Zakayo_calmDown1" subnet is designated to be the public subnet, while "Zakayo_calmDown2" is configured to be the private subnet. These distinctions in subnet types allow for a tailored and secure network architecture within the "Zakayo" Virtual Private Cloud (VPC).


## Step 3 : Creating an Internet Gateway

To ensure that our public resources have access to the internet, it's essential to add an Internet Gateway. This component facilitates communication between the resources within your Virtual Private Cloud (VPC) and the broader internet, enabling seamless connectivity for public-facing services and applications.

Navigate to the left side and select "Internet Gateway." While there may be a default Internet Gateway present, for our specific needs, we will create a dedicated one to facilitate communication between our resources within the Virtual Private Cloud (VPC) and the internet. Choose the "Create Internet Gateway" button located at the top right of the Internet Gateways section.

![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC%20aws/Default%20IG.png)

Enter the desired name for your Internet Gateway and proceed by selecting the "Create Internet Gateway" button located at the bottom right of the page. This action completes the setup, providing you with a dedicated Internet Gateway.

![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC%20aws/Create%20IG.png)


Even with the Internet Gateway created, it's important to note that your Virtual Private Cloud (VPC) cannot access the internet until the Internet Gateway is attached. To establish this connection, you must proceed to attach the newly created Internet Gateway to your VPC.

Choose the recently created Internet Gateway, then at the top right corner, click on "Actions," and from the dropdown menu, select "Attach VPC." In my case, "Zakayo-IG" is my internet gateway.

![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC%20aws/Attach%20IG%20to%20VPC.png)

Select the vpc to attach to. In my case "Zakayo" and select the "Attach Internet Gateway Option".

![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC%20aws/Attach%20IG%20to%20%20VPC2.png)

Well done!!! Your VPC can acccess the internet. Hurraayy!!!

## Step 4 : Creating a NAT Gateway

A Network Address Translation (NAT) Gateway serves the purpose of allowing private subnets within a Virtual Private Cloud (VPC) to access thi internet securely.

To create one navigate to the left side and select "NAT Gateways." While there may be default NAT Gateways present, for our specific needs, we will create a dedicated one to facilitate outbound communication from resources within the Virtual Private Cloud (VPC) to the internet. Choose the "Create NAT Gateway" button located at the top right of the NAT Gateways section.

![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC%20aws/Create%20NAT.png)

Fill in the required details. For my case I have named my NAT gateway "Zakayo-NATgw". 

![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC%20aws/NAT%20Settings.png)

Network Address Translation (NAT) Gateways are typically associated with public IP addresses. The primary purpose of NAT is to enable private network resources to communicate with the public internet. An Elastic IP (EIP) is a static, public IPv4 address in cloud environments. Its primary purposes include providing a consistent public-facing address for instances or resources, ensuring high availability by allowing quick remapping to other instances, and reducing DNS propagation time when changing public IP addresses associated with services. Elastic IPs are particularly useful for internet-facing resources in dynamic cloud environments where instances may be started, stopped, or replaced.

After associating the NAT Gateway with the private route table, the details for the NAT Gateway should reflect the specific configuration you have set. This may include information such as the associated Elastic IP address, the subnet in which the NAT Gateway is located, and any relevant status indicators.

![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC%20aws/NAT%20details.png)

You're doing great! Lets take the next step...

## Step 5 : Creating Route Tables

Route tables provide the necessary framework for managing and controlling network traffic within a VPC. They are essential for customizing network paths, ensuring connectivity to the internet, facilitating communication between different subnets, and maintaining a secure and efficient network infrastructure. To effectively manage network traffic within your Virtual Private Cloud (VPC), it's crucial to create separate route tables for both public and private resources. This segregation allows you to customize routing rules as well as control internet access.

To create dedicated route tables for our network configuration, navigate to the "Route Tables" section on the left. Once selected, you'll observe the presence of default route tables. However, for our specific requirements, we'll proceed to create customized route tables to tailor the routing rules for both public and private resources. Choose the "Create Route Table" button located at the top right of the Route Table section. 

![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC%20aws/Default%20RT.png)


Enter the desired name for your Route Table  and proceed by selecting the "Create Route Table " button located at the bottom right of the page.

![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC%20aws/Create%20RT.png)


![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC%20aws/Successfully%20created%20RT.png)

In my case, I've created two Route Tables named "Zakayo_RT-1" and "Zakayo_RT-2,"  The "Zakayo_RT-1"  is designated to be the public Route Table, while "Zakayo_RT-2" is configured to be the private Route Table.

![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC%20aws/My-RTs.png)

To establish the desired network configuration, it's essential to associate route tables with the corresponding subnets. Specifically, the public route table should be linked with the public subnet, while the private route table should be associated with the private subnet. This ensures that routing rules are aligned with the nature of the resources within each subnet, optimizing the network setup for both public and private components.

To create associations between route tables and subnets, select the desired subnet. On the top right corner, next to "Create Route Table," click on "Actions." From the dropdown menu, choose "Edit Subnet Associations." This process enables you to establish the connection between the selected subnet and the intended route table, aligning routing rules with the subnet's purpose, be it for public or private resources.

![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC%20aws/Associate%20RTs%20with%20subnets.png)

After completing the association process, you will notice the "Explicit Subnet Associations" section, showing the subnets associated with their respective route tables. This section provides a quick reference to confirm that the routing configurations align with the intended purpose of each subnet, whether designated for public or private resources. For my case "Zakayo_RT-1" is my public Route Table and is associated with "Zakayo_calmDown1" subnet which is the public subnet

![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC%20aws/Successfull%20RT-subnet%20Association.png)


Given that you have public subnets where an Internet Gateway is in use, it's crucial to configure routes in the public route table to enable internet access for resources within those subnets. Typically, you'd add a default route (0.0.0.0/0) pointing to the Internet Gateway in the public route table, ensuring that traffic destined for the internet is properly directed. This setup allows public-facing resources to communicate with external services on the internet.

To add a route in your route table, select the route table, then at the top right corner, next to "Create Route Table," click on "Actions." From the dropdown menu, choose "Edit Routes." This allows you to modify routes and specify how traffic should be directed.

![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC%20aws/Add%20route%20to%20privateRT%20and%20indicate%20its%20from%20IG.png)

For the public route table "Zakayo_RT-1," I will add a route where the destination is "0.0.0.0/0" and the target is the Internet Gateway "Zakayo_IG". With this route configuration resources within the public subnet can have internet access. 

![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC%20aws/Add%20route%20to%20public%20RT%20and%20indicate%20its%20from%20IG.png)

Let's look at "Zakayo_RT-1" Route Table Details

![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC%20aws/RT1%20details.png)

For the private route table "Zakayo_RT-2," I will add a route where the destination is "0.0.0.0/0" and the target is the NAT Gateway "Zakayo_NATgw". This route configuration allows resources within the private subnet to access the internet securely through the NAT Gateway.


![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC%20aws/select%20NAT%20created%20earlier.png)


Let's look at "Zakayo_RT-2" Route Table Details

![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC%20aws/RT2%20details.png)


## Step 6 : Creating a Security Group

A Security Group in cloud computing, particularly within AWS (Amazon Web Services), is a fundamental component for controlling inbound and outbound traffic to and from instances (virtual servers). We will look at instances in a later project.

To create a security group, navigate to the "Security Groups" section on the left. Once selected, you'll observe the presence of default security groups. However, for our specific requirements, we'll proceed to create customized security groups to define inbound and outbound traffic rules for both public and private resources. Choose the "Create Security Group" button located at the top right of the Security Groups section.

![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC%20aws/Default%20Security%20Group.png)

Fill in the basic details

![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC%20aws/Create%20Security%20Group.png)

We will define inbound rules, specifying the types of incoming traffic permitted for resources associated with this security group. For this particular case, I will add SSH and HTTP.

![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC%20aws/Add%20inbound%20rules.png)

The outbound rules, which define the types of outgoing traffic allowed from the resources associated with the security group therefore  they remain unchanged.

![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC%20aws/Outbound%20remain%20as%20is.png)

Once all the details, including inbound rules for SSH and HTTP, are configured, click on the "Create Security Group" button at the bottom to finalize

![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC%20aws/Create%20SG.png)

And here is the successfully created security group: "Zakayo-SG".

![Alt Text](https://github.com/WinnieKiarago/AWS-Cloud-Projects/blob/main/VPC%20aws/SG%20successfully%20Created.png)

Excellent! The VPC and its components have been successfully created. 





