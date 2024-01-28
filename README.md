# Elastic-Load-Balancing-ELB- (Network Load Balancer)
Creating a Elastic Load Balancing (ELB)  
 They enable you to achieve greater fault tolerance in your applications and seamlessly provide the correct amount of load balancing capacity needed in response to incoming application requests.

![image](https://github.com/kalejcamto/Elastic-Load-Balancing-ELB-/assets/101201140/e9f9029f-146f-4241-8694-a8757fcb804b)

Types of Load Balancer
![image](https://github.com/kalejcamto/Elastic-Load-Balancing-ELB-/assets/101201140/e05a802f-fed2-45e7-8d25-cc3ab2da883d)

ELB detects unhealthy instances within a pool and automatically reroutes traffic to healthy instances until the unhealthy instances have been restored. Elastic Load Balancers can be enabled within a single Availability Zone or across multiple zones for greater consistent application performance.

![image](https://github.com/kalejcamto/Elastic-Load-Balancing-ELB-/assets/101201140/27225405-c242-49f3-9019-2db5c466e5e6)

I created a Network Load Balancer
Notice that the default listener is TCP port 80 which is used for serving HTTP traffic.

![image](https://github.com/kalejcamto/Elastic-Load-Balancing-ELB-/assets/101201140/aad6d04e-2789-4e65-aa7f-21efb1d58929)
Security Group created on previous repository 

![image](https://github.com/kalejcamto/Elastic-Load-Balancing-ELB-/assets/101201140/818cfe32-b66c-44cd-954b-f2be2d43aeeb)

![image](https://github.com/kalejcamto/Elastic-Load-Balancing-ELB-/assets/101201140/a6e61030-2e56-4e73-bd7e-463637843950)

![image](https://github.com/kalejcamto/Elastic-Load-Balancing-ELB-/assets/101201140/65d10be1-c1b4-489c-902a-85a64e8884f8)

Ensure you set the protocol to TCP. Because network load balancers operate at layer 4 and aren't HTTP aware, if you set the protocol as HTTP you will be unable to use the target group with your network load balancer. 
![image](https://github.com/kalejcamto/Elastic-Load-Balancing-ELB-/assets/101201140/1f178c08-54e1-4af0-a6b4-8b9cc2acaa0f)
At the bottom of the page, click Create target group.
![image](https://github.com/kalejcamto/Elastic-Load-Balancing-ELB-/assets/101201140/f03f0ebd-c134-4a33-9bf9-0a332ca50c45)
The message is due to not creating an Auto Scaling group or launching any EC2 instances yet. That is not a problem. You will configure your Auto Scaling group to register its EC2 instances in the Network Load Balancer's target group.

![image](https://github.com/kalejcamto/Elastic-Load-Balancing-ELB-/assets/101201140/fa065a62-ffb7-47f0-8f3d-b4de18d3dbbf)

Return to your load balancer configuration browser tab.
![image](https://github.com/kalejcamto/Elastic-Load-Balancing-ELB-/assets/101201140/581f8e28-78a6-4097-8626-f56d09e0f987)

Ready to create a load balancer
![image](https://github.com/kalejcamto/Elastic-Load-Balancing-ELB-/assets/101201140/e26c6c62-0705-4282-968a-355e17b41a91)


Done 
![image](https://github.com/kalejcamto/Elastic-Load-Balancing-ELB-/assets/101201140/3ebe2156-9b58-468f-933e-5f1a94ad1e18)

![image](https://github.com/kalejcamto/Elastic-Load-Balancing-ELB-/assets/101201140/3a0370d4-cce1-4b76-91c3-ce16a096f2ad)

![image](https://github.com/kalejcamto/Elastic-Load-Balancing-ELB-/assets/101201140/ccf250b2-af5d-4b72-a6ab-b8a4c4f5ce7a)

![image](https://github.com/kalejcamto/Elastic-Load-Balancing-ELB-/assets/101201140/0d8d49d5-a5e4-4d65-b150-b6381c9bb97d)

In the left-hand menu, click Target Groups, on the Website target group and edit "web":
![image](https://github.com/kalejcamto/Elastic-Load-Balancing-ELB-/assets/101201140/cc197eea-b0fd-4451-8f25-612e15f01c99)

I go to Target deregistration management and set it up for 30 sec and saved it. 

## Summary
## In this lab step, I created a Network Load Balancer with a target group ready to service HTTP requests on port 80. This load balancer will be used as the front-end to a website. The website will run on EC2 instances that are created via an Auto Scaling group. This is a very common use case.


# Creating Auto Escaling: 

 In the left-hand menu, click Auto Scaling Groups:
 ![image](https://github.com/kalejcamto/Elastic-Load-Balancing-ELB-/assets/101201140/a1697495-f705-49e9-940c-f0edd31ae3cc)
In the Launch template field, select webserver-cluster:

![image](https://github.com/kalejcamto/Elastic-Load-Balancing-ELB-/assets/101201140/b0a79fab-8ba8-42e1-bea3-fdafba0f4146)
To advance to the next page of the wizard, click Next:


![image](https://github.com/kalejcamto/Elastic-Load-Balancing-ELB-/assets/101201140/a17ccc59-07fe-4114-a570-79ac0a201079)

 ![image](https://github.com/kalejcamto/Elastic-Load-Balancing-ELB-/assets/101201140/16650a13-b76d-467f-a2a6-602dae8a279b)

You will see a wizard step that allows you to configure notifications when scaling events occur. Notifications aren't used in this lab.

![image](https://github.com/kalejcamto/Elastic-Load-Balancing-ELB-/assets/101201140/63d75d96-3867-4a39-aef9-cbde8557ef86)



![image](https://github.com/kalejcamto/Elastic-Load-Balancing-ELB-/assets/101201140/970d2a65-8ede-4018-9577-680732df4f2e)



 

