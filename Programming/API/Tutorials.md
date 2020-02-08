---
modified: 2020-01-30T23:05:36+05:30
---

- [APIs for Beginners](https://www.youtube.com/watch?v=GZvSYJDk-us&t=766s)
<<<<<<< HEAD
- [RESTful API](https://www.youtube.com/watch?v=Q-BpqyOT3a8)


## What is stateless:

Let’s say, you have 2 Web-Servers with 2 separate IP’s. They both have their own DB, which is kept synchronous.

Now, a customer connects to your website and your load-balancer sends him to Server1 - he logs in, and wants to check his messages. But when he’s opening his inbox, this new request is being sent to Server2 (thanks to your load-balancer). But you’re not logged in on Server2 - so, it’ll send you back to the login-screen -> bad user-story…

In a stateless environment, you always send along all the information needed, to finish some task - thats how just any endpoint would be able to also serve you with that task… Then it also doesn’t matter, which server would open your inbox.
  
=======
- [RESTful API](https://www.youtube.com/watch?v=Q-BpqyOT3a8)
>>>>>>> 6a3477f6cd207ede374c2498fd720fad9de478bf
