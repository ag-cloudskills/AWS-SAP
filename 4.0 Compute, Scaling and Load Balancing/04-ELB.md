# ELB

![ELB architecture](/4.0%20Compute,%20Scaling%20and%20Load%20Balancing/04.1-ELB-arch.drawio.svg)
  
- ELB can be internet facing or internal
- ELB are configured with listners which accepts traffic on a port and protocol
- It needs minimum 8 free ip for the LB (/27 subnet)
- Internet facing ELB can access private EC2 instances
- Each ELB is configured with A record DNS name
- cross zone LB - better distribution of load
- v1( migrate) and v2 ( prefer) LB
- classic lb ( v1), not 7 layer , 1 SSL per CLB
- ALb v2 - http,https,websocket
- NLB v2 - tcp,tls and udp
- v2 support target groups and rules  

testing PR process

## User Session state

- unique interaction with application, data is held within session
- it can be of min, hour or days
- Stateless - if this is stored externally out of the application
- a very important feature for the user experience


## ALB vs NLB

### ALB

- layer 7 - http or https
- type of content , cookies, custom header
- SSL terminated at LB and then new connection is created
- ALB must have ssl for https
- slower than NLB
- can evaluate health check
- rules are configured at listner and processed in priority order
- default is captured at last
- rules conditions can be - host-header, http-header, http-request-method, path-pattern, query-string & source-ip
- actions - forward, redirect, fixed-response, authenticate-oidc & authenticate-cognito

#### Connection Stickiness

- enable stickiness on ALB  which generates cookie ( 1 s to 7 days)
- cookie locks the device to a single backend instance for a duration
- cookie expire or cookie failure( instance failure)result in a new backend instance
- Stickiness can cause uneven load

### NLB

- layer 4 - tcp, tls, udp , tcp_udp
- no header, no cookies, no session stickiness
- very fast
- non-web applications
- health check - ICMP/TCP handshake
- static Ip-useful for whitelisting
- unbroken encryption
- used with private link


### Connection Draining ( Classic LB only)

- it allows in-flight requests to complete
- timeout value between 1 and 3600 seconds ( default 300)
- InService: Instance deregistation curretly in progress

### Deregistration Delay

- defined on target group
- existing connections can continue till it is completed naturally or deregistration delay is reached
- enabled by default  ( 0-3600 seconds)

### X-FORWARDED-FOR

- HTTP Header  ( layer 7)
- header is added or appended

### Proxy protocol

- layer4(tcp)
-  