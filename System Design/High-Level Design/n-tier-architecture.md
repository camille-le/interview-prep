## N-Tier Architecture
N-tier architecture divides an app into logical layers and physical tiers, where each layer has a specific responsibility.
* Tiers are physically separated, running on separate machines
* A tier can call to another tier or use asynchronous messaging

Some examples of n-tier architecture include:
![N-tier architecture](https://raw.githubusercontent.com/karanpratapsingh/portfolio/master/public/static/courses/system-design/chapter-III/n-tier-architecture/n-tier-architecture.png)
[Image Source](https://raw.githubusercontent.com/karanpratapsingh/portfolio/master/public/static/courses/system-design/chapter-III/n-tier-architecture/n-tier-architecture.png)

* 1-Tier
  * Running app on a personal computer; all required components are a single application or server
* 2-Tier
  * Presentation Layer: Runs on the client 
  * Data Access Layer: Presentation layer communicates with the data store
* 3-Tier
  * Presentation Layer: Handles user interactions with the app
  * Business Logic Layer (Application Tier, Logic Tier, Middle Tier): Accepts data from the app layer, validates it as per business logic and passes it to the data layer
  * Data Access Layer (Data Tier): Receives data from the business layer and performs the necessary operation on the DB



| Pros                                               | Cons                                                    |
|----------------------------------------------------|---------------------------------------------------------|
| Can improve availability.                          | Increased complexity of the system as a whole.           |
| Better security as layers can behave like a firewall. | Increased network latency as the number of tiers increases. |
| Separate tiers allow us to scale them as needed.   | Expensive as every tier will have its own hardware cost. |
| Improve maintenance as different people can manage different tiers. | Difficult to manage network security.                  |
#### Sources
- [System Design Primer](https://github.com/karanpratapsingh/system-design)