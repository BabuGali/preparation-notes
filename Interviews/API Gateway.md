- API Gateways serve as **a singular entry point for processing all API requests**
- it features Traffic management, security protocols, caching and monitoring that allow the effective management, optimization and safeguarding of APIs.
- An API Gateway acts as a mediator between client applications and backend services in microservices.
- Some key responsibilities handled by a microservices API gateway
	- **Traffic Management** - An API gateway manages incoming requests and routes them based on key factors such as request path, headers, and query parameters, among others. It allows for efficient distribution of traffic and ensures proper load balancing among target endpoints
	- - Transformation - Protocol translation, response formatting, etc.
	- Caching
	- Load Balancing
	- Observability - Logging, monitoring and tracing
	- Authentication
	- Rate-limiting - t is a technique used to control the amount of traffic that may flow through an API gateway. By limiting the number of requests that can be made within a specific time period, we can ensure that our API can still function properly even under heavy load.
- Protocol Translation - For example, an API gateway can translate HTTP requests into WebSockets or gRPC requests, enabling API clients to communicate with backend services that use different protocols.
- How do you avoid single point of failure in API gateway?
	- you can **use a combination of availability zones and multi-region deployments**.
- Examples
	- Open Source
		- Netflix API gateway (Zuul)
		- Kong API gateway
		- Express Gateway
		- Spring cloud API gateway
	- Proprietary 
		- Amazon API gateway
		- Apigee
		- Azure API gateway
	- 
- Zuul is a JVM-based router and server-side load balancer from Netflix. Netflix uses Zuul for the following: **Authentication**. **Insights**