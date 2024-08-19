# Golang Load Balancer
This project implements a load balancer which is a necessicity in todays internet era. Modern webistes might have to deal with hundreds of thousands of requests and thus it's important to route traffic to the suitable server so that the underlying infrastructure can handle the traffic and keep on its buisness ongoing. 
<br>
## Overview
A load balancer is a tool that is commonly used to coordinate the volume of traffic between the available servers.
A load balancer sits in front of a group of servers which is referred to as Serverpool, and the load distribution is performed based on various load balancing algorithms. 

## Features
* Weighted Round-Robin Scheduling Algorithm: The load balancer uses the Weighted Round-Robin (WRR) algorithm to distribute traffic. This algorithm assigns weights to each server, allowing the load balancer to prioritize servers based on their capacity or performance. It ensures that healthier backends with available capacity receive more requests.
* Health Checks: The load balancer continuously monitors the health of the backend servers, ensuring that traffic is only directed to servers that are capable of handling requests.
<br>

The input is given through the configuration file `config.yaml`. You can change it as per your requirements
``` yaml
//port in which load balancer will be running
lb_port: 3000
//available backend servers
backends:
  - url: "http://localhost:5100"
    weight: 5
  - url: "http://localhost:5200"
    weight: 3
  - url: "http://localhost:5300"
    weight: 4
  - url: "http://localhost:5400"
    weight: 1
  - url: "http://localhost:5500"
    weight: 2

```

## Future Works
* Implement the various other scheduling algorithms
* Add some security measures 


## References
* ([load_balancer](https://github.com/leonardo5621/golang-load-balancer/tree/master))
* ([simplelb](https://github.com/kasvith/simplelb))
