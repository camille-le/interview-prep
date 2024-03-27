## Queues

![Queues](https://media.licdn.com/dms/image/D4E22AQEF8dl6e6_Y-g/feedshare-shrink_800/0/1701104695210?e=1714608000&v=beta&t=ZgsYc1y5RC6s-m8YwexlLrx8ZzTLnNfwokEETIs6gpQ)


1. Simple FIFO Queue
A simple queue follows FIFO (First In First Out). An new element is inserted at the tail of the queue, and an element is removed from the head of the queue.

If we would like to send out email notifications to the users whenever we receive a payment response, we can use a FIFO queue. The emails will be sent out in the same order as the payment responses.

![Message Queue](https://res.cloudinary.com/practicaldev/image/fetch/s--_jJoQnjF--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_800/https://raw.githubusercontent.com/karanpratapsingh/portfolio/master/public/static/courses/system-design/chapter-III/message-queues/message-queue.png)


2. Circular Queue
A circular queue is also called a circular buffer or a ring buffer. Its last element is linked to the first element. Insertion takes place at the front of the queue and deletion at the end of the queue.

A famous implementation is LMAX’s low-latency ring buffer. Trading components talk to each other via a ring buffer. This is implemented in memory and super fast.

3. Priority Queue
The elements in a priority queue have predefined priorities. We take the element with the highest (or lowest) priority from the queue. Under the hood, it is implemented using a max heap or a min heap where the element with the largest or lowest priority is at the root of the heap.

A typical use case is assigning patients with the highest severity to the emergency room while others to the regular rooms.

4. Deque
Deque is also called double-ended queue. The insertion and deletion can happen at both the head and the tail. Deque supports both FIFO and LIFO (Last In First Out), so we can use it to implement a stack data structure.



#### Source 
* ByteByteGo / Alex Xu 
* https://dev.to/karanpratapsingh/system-design-message-queues-k9a