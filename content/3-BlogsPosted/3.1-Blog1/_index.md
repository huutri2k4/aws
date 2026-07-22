---
title: "Blog1"
date: 2026-07-09
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

# Building a Dual-Token Authentication System for Nakama Game Server Using Amazon Cognito on AWS.

### INTRODUCTION
In online gaming, authentication systems must not only guarantee robust security but also deliver a seamless login experience. Nakama utilizes Session Tokens to manage gameplay sessions, while Amazon Cognito issues JWTs (JSON Web Tokens) to verify user identity. If these two platforms operate independently, players might have to authenticate multiple times or encounter workflow disruptions during gameplay.

The Dual-Token Authentication solution integrates Amazon Cognito and Nakama to fully decouple identity management from gameplay session control. Cognito is responsible for user authentication, whereas Nakama generates and oversees Session Tokens via a Go Runtime Hook, maintaining system security while ensuring a smooth user experience.

### Macro Architecture
The infrastructure layout utilizes core services including Amazon Cognito, Amazon CloudFront, an Application Load Balancer (ALB), a Network Load Balancer (NLB), and Nakama containers deployed on Amazon ECS Fargate.

The operational workflow behaves as follows:
1. The player authenticates using Amazon Cognito.
2. Cognito returns a verified JWT Access Token.
3. The game client forwards the JWT to Nakama via Amazon CloudFront.
4. The Go Runtime Hook validates the JWT payloads and issues a Nakama Session Token.
5. All downstream system requests utilize this Nakama Session Token.

This architectural blueprint successfully decouples user identity tracking from persistent active gameplay session states.

### Authentication Workflow
First, the player logs in with Amazon Cognito via the `USER_SRP_AUTH` protocol, which ensures that passwords are never transmitted directly over the network to the server. Upon successful authentication, Cognito issues a signed JWT containing vital claim parameters such as `sub`, `iss`, `exp`, and `client_id`.

Once the JWT hits the Nakama server, the Go Runtime Hook audits the cryptographic digital signature, expiration timestamps, Issuer domain, and matching Client IDs. If the incoming token is valid, Nakama initializes a native Session Token for the player to utilize throughout their entire gaming session.

### The Role of ALB and NLB
The architecture simultaneously deploys two distinct Load Balancer types to handle diverse networking traffic profiles:
* **Application Load Balancer (ALB):** Manages inbound HTTP APIs, strictly permitting predefined routing paths while automatically deflecting invalid or unauthorized attempts with a standard `403 Forbidden` status code.
* **Network Load Balancer (NLB):** Governs stateful WebSocket data pipes at Layer 4 (TCP layer), preserving network packet stability and ensuring ultra-low latency metrics necessary for real-time competitive gaming execution.

### Perimeter Security Controls
Amazon CloudFront serves as the absolute singular HTTPS public ingress gateway, integrating with **AWS WAF** to inspect, filter, and drop malicious payloads before they ever reach downstream backend server infrastructure.

Additionally, the embedded Go Runtime Hook rejects unverified tokens and strictly references the verified `sub` (Subject) value inside the payload to map player profiles, completely mitigating identity spoofing vectors. Stateful **Security Groups** are narrow-mapped to mandate that network traffic strictly flows along the verified line-of-rate route extending from CloudFront down into Nakama target tasks.

### Conclusion
The integrated Dual-Token Authentication solution seamlessly combining Amazon Cognito and Nakama delivers a highly secure, adaptive, and scalable framework tailored for contemporary online multiplayer architectures. Backed by CloudFront, ALB, NLB, and serverless Amazon ECS Fargate tasks, the environment scales up security posture while offering elastic throughput performance capable of driving real-time persistent WebSocket configurations.

...
offering elastic throughput performance capable of driving real-time persistent WebSocket configurations.

![Nguyen Huu Tri](/aws/images/tri.jpg)

**Reference Source:** <https://aws.amazon.com/blogs/architecture/dual-token-authentication-for-nakama-game-servers-with-amazon-cognito-on-aws/>