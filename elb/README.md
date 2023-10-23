# ELB - Elastic Load Balancing

- Elastic Load Balancing (ELB) automatically distributes incoming application traffic across multiple targets (EC2 / Containers) in one or more Availability Zones (AZs). 
- [AWS Documentation](https://aws.amazon.com/elasticloadbalancing/)

    - Classic Load Balancer (Deprecated)
    - Application Load Balancer (supports HTTP, HTTPS, Websocket)
    - Network Load Balancer (supports TCP, TLS(secure TCP), UDP)
    - Gateway Load Balancer (Operates at Network Layer - layer 3, IP Protocol)


## ALB - Application Load Balancer
- Works on Layer 7 (Application Layer)
- Supports HTTP, Websocket
- Support redirects to multiple HTTP applications across target groups
- Support redirects to multiple applications on same machine

### Target Groups Can be
- Ec2 instances (can be managed by an Auto scaling group) - HTTP
- ECS Tasks (managed by ECS itself) - HTTP
- Lambda functions - HTTP request is translated into a JSON Event
- IP Addresses - must be private IPs 

###  ALB - Routing Table to different target group
- based on url path -> ex:  mydomain.com/resource1 & mydomain.com/resource2
- based on hostname in url -> ex: mydomain1/com & mydomain2.com
- based on querystring, headers -> ex: mydomain.com?id=1 & mydomain.com?id=2

[ALB Hands on Article Medium](https://hkcodeblogs.medium.com/scaling-with-aws-1-application-load-balancer-alb-b9ea2edb5f46)