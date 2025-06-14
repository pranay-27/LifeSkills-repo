# Scaling and Load Balancing

## Load Balancing

A load balancer takes all the incoming requests and spreads them across multiple servers instead of sending everything to just one. This way, no single server gets overloaded, and the system runs more smoothly.

### Different Ways to Load Balance

**Round Robin**
Send each new request to the next server in line.

**Limited Connections**
Looks at which server has the fewest active connections and sends the new request there.

**IP Hash**
Uses the user's IP address to decide which server they always go to. Keeps things consistent for each user.

Some popular tools for this are **NGINX**, **HAProxy**, and if you're on **AWS**, their **Elastic Load Balancer (ELB)** works well.

---

## Scaling Up vs Scaling Out

### Vertical Scaling

This is when you upgrade your existing server—more RAM, better CPU, faster storage, etc. It's easy to do and delivers quick results. The downside is you eventually hit physical limits.

### Horizontal Scaling

Instead of making one server stronger, you add more servers to share the workload. It takes more planning but is very useful in the long term. Plus, if one server fails, others keep things running.

Modern apps, especially those using microservices, benefit more from horizontal scaling.

---

## My Advice

I think we should definitely set up a **load balancer** first—that'll help with our current issues. Then we can start thinking about adding more servers instead of just upgrading the one we have.

A few other things that may help:

* Try to make the app **stateless** where possible—this makes scaling easier.
* Use **Docker** containers to improve deployment and portability, and consider **Kubernetes** if we want auto-scaling.
* Set up **monitoring tools** so we can track when we're nearing capacity.

---

## Conclusion

Getting a load balancer running with a few servers can fix our performance headaches and set us up nicely for growth. The whole system becomes more stable since we're not depending on just one machine, and users should notice faster response times too.
