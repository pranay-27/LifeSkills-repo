# Scaling and Load Balancing

## Load Balance:

A load balancer takes all the incoming requests and spreads them across multiple servers instead of throwing everything on just one server. This way no single server gets complicated and everything runs easily.

Different ways to do this:

**Round Robin** - Send each new request to the next server in line.

**Limited Connections** - Looks at which server has the fewest people connected and sends the new request there.

**IP Hash** - Uses the user's IP address to decide which server they always go to. Keeps things consistent for each user.

Some popular tools for this are NGINX, HAProxy, and if you're on AWS then their Elastic Load Balancer works well.

## Scaling Up vs Scaling Out

**Vertical Scaling**
This is when you just update your existing server - more RAM, better CPU, faster storage, etc. It's  easy to do and see results quickly. The problem here is you can upgrade before you hit physical limits.

**Horizontal Scaling**  
Instead of making one server stronger, add more servers to share the work. It takes more planning but it is very useful in long term. Plus if one server dies, you've got others to keep things running.

For modern apps, specially when we use microservices gets more benefits when we use horizotal scaling.

## My Advices

I think we should definitely get a load balancer set up first - that'll help with our current issues. Then we can start thinking about adding more servers instead of just upgrading the one we have.

A few other things that may help:
- Better try to make the app stateless where possible, makes scaling easier.
- Docker containers could be useful to get more benefits, and Kubernetes if we want to use with auto-scaling.
- If possible set up some monitoring so we may know when we're getting close to capacity.

## conclusion

Getting a load balancer running with a few servers can fix our performance headaches and set us up nicely for growth. The whole system becomes more stable since we're not depending on just one machine, and users should notice faster response times too.
