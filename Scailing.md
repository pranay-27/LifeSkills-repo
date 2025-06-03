# Scaling and Load Balancing

## Load Balancer

A load balancer used to  divide the incoming traffic equally to multiple servers and  put all the load on one. This avoids overload and improves performance.

### Common Load Balancing Methods

- **Round Robin** – Sends requests one by one to all server.
- **Least Connections** – Sends traffic to the server with the less number of active users.
- **IP Hash** – Routes the request based on the user's IP to a specific server.

### Useful Tools

- NGINX  
- HAProxy  
- AWS Elastic Load Balancer (ELB)

---

## Vertical vs Horizontal Scaling

### Vertical Scaling

- Upgrade the same server with more CPU, RAM, etc.
- Easier and faster to do.
- Has a limited ports physically.

### Horizontal Scaling

- Add more servers to handle traffic
- Better for long-term growth
- No single point of failure
- Works best with  applications or microservices

---

## Suggestion

- Start using a load balancer to split the traffic
- Move towards horizontal scaling for better performance and availability
- Make parts of the application stateless for easier scaling
- Use tools like **Docker** and **Kubernetes** for container management and auto-scaling
- Set up monitoring to know when scaling is needed

---

## Conclusion

When we add a load balancer across our application with multiple servers, we'll solve the current performance problems and be ready to handle more users. This approach will also make our application works more fast as it won't depend on just one server, and users will experience faster response times.
