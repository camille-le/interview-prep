## N-Tier Architecture
N-tier architecture divides an app into logical layers and physical tiers, where each layer has a specific responsibility.
* Tiers are physically separated, running on separate machines
* A tier can call to another tier or use asynchronous messaging

![N-tier architecture](https://raw.githubusercontent.com/karanpratapsingh/portfolio/master/public/static/courses/system-design/chapter-III/n-tier-architecture/n-tier-architecture.png)
[Image Source](https://raw.githubusercontent.com/karanpratapsingh/portfolio/master/public/static/courses/system-design/chapter-III/n-tier-architecture/n-tier-architecture.png)

Some examples of n-tier architecture include:
* **1-Tier**
  * Running app on a personal computer; all required components are a single application or server
- **2-Tier**
  - Original client-server model.
  - Presentation Layer: Executes on the client side.
  - Data Access Layer: Direct communication with the data store.
* **3-Tier**
  * Presentation Layer (User-Interface): 
    * Handles user interactions with the app
    * Display information to and collect info from the user
    * User Interface (HTML/CSS/JavaScript)
  * Business Logic Layer (Application Tier, Logic Tier, Middle Tier): 
    * Accepts data from the app layer, validates it as per business logic and passes it to the data layer
    * Communicates with the Data Tier using API calls
    * Where Data is Processed (Python, Java, PHP or Ruby)
  * Data Access Layer (Data Tier): 
    * Receives data from the business layer and performs the necessary operation on the DB
    * Where info processed by the app is stored and managed
    * Where Data is Stored and Managed (PostgreSQL, MySQL, MongoDB...)

In web development, the corresponding tiers are: web server (presentation), application server (middle tier) and database server (backend tier of a a web app).
  
| Pros                                               | Cons                                                    |
|----------------------------------------------------|---------------------------------------------------------|
| Can improve availability.                          | Increased complexity of the system as a whole.           |
| Better security as layers can behave like a firewall. | Increased network latency as the number of tiers increases. |
| Separate tiers allow us to scale them as needed.   | Expensive as every tier will have its own hardware cost. |
| Improve maintenance as different people can manage different tiers. | Difficult to manage network security.                  |

Per IBM, other benefits of a three-tier architecture include:
1. Each tier runs on its own infrastructure
2. Each tier can be developed simultaneously by a separate development team
3. Each tier can be updated or scaled as needed without impacting the other tiers

#### Sources
- [IBM: Three-Tier Architecture](https://www.ibm.com/topics/three-tier-architecture)
- [System Design Primer](https://github.com/karanpratapsingh/system-design)
