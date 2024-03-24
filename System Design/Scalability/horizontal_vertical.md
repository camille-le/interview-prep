## Scalability
Scalability refers to how a system responds to changes by adding or removing resourceds to meet demands.
![Vertical vs Horizontal Scaling Compared](https://crl2020.imgix.net/img/vertical-versus-horizontal-scaling-compared-diagram.png?auto=format,compress&max-w=640)
*Image credit: [Vertical vs Horizontal Scaling Compared](https://crl2020.imgix.net/img/vertical-versus-horizontal-scaling-compared-diagram.png?auto=format,compress&max-w=640)*

### Horizontal Scaling ("Scaling Out")
- Add more machines to expand a system's scale
- By adding more instances to the existing pool of servers, load can be distributed more evenly

| Pros                   | Cons                                  |
|------------------------|---------------------------------------|
| Increased redundancy   | Increased complexity                  |
| Better fault tolerance | Data inconsistency                    |
| Flexible and efficient | Increased load on downstream services |
| Easier to upgrade      |                                       |

### Vertical Scaling ("Scaling Up")
- Add more power to an existing machine 
- Increase hardware capacity

| Pros                | Cons                               |
|---------------------|------------------------------------|
| Simple to implement | Risk of high downtime              |
| Easier to manage    | Harder to upgrade                  |
| Data consistent     | Can be a single point of failure   |

#### Sources
- [System Design Primer](https://github.com/karanpratapsingh/system-design)
