# Interview Prep

## Leetcode Resources
Lorem ipsum

## System Design Resources
- [Design Docs at Google](https://www.industrialempathy.com/posts/design-docs-at-google/)
- [Latency Measurement - Igor](https://igor.io/latency/)  
- [Everything You Know About Latency Is Wrong - BraveNewGeek](https://bravenewgeek.com/everything-you-know-about-latency-is-wrong/)
- [Content Delivery Networks - web.dev](https://web.dev/articles/content-delivery-networks)
- [System Design Primer](https://github.com/karanpratapsingh/system-design)

https://github.com/donnemartin/system-design-primer?
https://www.youtube.com/playlist?list=PLrtCHHeadkHp92TyPt1Fj452_VGLipJnL
https://www.quora.com/What-should-a-new-grad-know-in-order-to-perform-well-on-system-design-interviews

Read Design of Data-Intensive applications.



Keep a list of points to cover ready which you'll go through for most of the problems - like overall architecture, data size estimates, algorithms to cover, data model, database to use, scalability etc. This helps so that you don't forget any points and also don't get stuck with awkward pauses and are able to drive the interview on your terms.

Practice by giving more interviews and analyzing them later on. You can even apply for companies you don't want to go just for interview practice.

You can even keep a list of bullet points for most types of questions that are asked, and write them down in a notebook. In most cases with remote interviews, you can ask the interviewer to use a notebook for designing, and refer your points in case a similar question is asked (it is unethical though).

Study more. Not just design questions, but also the underlying concepts like distributed caching (redis), various db options (sql, document store, columnar db etc), messaging queues (kafka), load balancer, rate limiter etc.


## System Design Interview Framework
[1] Communication
- Describe problem at hand
- Communicate your thought process & plan of action 
- Identify requirements, capacity planning
- Identify use cases, edge cases, scope, data modeling, etc.
[2] High-Level Design 
- Anticipate and know what to do when a component fails 
- Reliability (Retrying, Data Loss)
- Availability (Load Balancing)
- Exception Handling
- Observability (Logging, Alerting)
- Service Platforms
[3] Scalability
- Database Choice
- Horizontal vs. Vertical Scaling
- Synchronous vs. Asynchronous
- Caching
- Data Redundancy, ...