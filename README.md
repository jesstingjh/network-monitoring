# network-monitoring
### Network Monitoring Project

**Tech Stack:** **Python**, **Gurobi Solver**, **Matplotlib**

In this project, I used **Python** and **Gurobi Solver** to optimize sensor placement in a water distribution network consisting of 811 sensors and 1123 pipes. By applying **optimization techniques** and modeling a range of constraints and objectives, I determined the best locations for sensors to effectively monitor the network for pipe bursts. **Matplotlib** was used to visualize the results and assess sensor placement outcomes.

The project approached the problem from a few angles:
- **Minimize the number of sensors required** to cover all pipes
- **Maximize the expected number of pipe bursts detected**, given each pipe's burst probability, while using up to b sensors
- **Place b sensors iteratively** in locations that maximize the detection of expected pipe bursts
- **Minimize the maximum criticality** of uncovered pipes by locating up to b sensors in high-priority areas

Throughout the project, I had to model a large number of constraints, which made it computationally intensive. To mitigate the risk of losing progress due to unexpected interruptions (such as timeouts or kernel crashes), I implemented **checkpointing**. This allowed the program to save intermediate results at critical stages, ensuring that the optimization could resume from the last saved checkpoint rather than restarting from scratch.

**Challenges & Solutions:**  
The complexity of managing numerous constraints was addressed by leveraging **Gurobi Solver**, which efficiently handled large-scale optimization tasks. The checkpointing mechanism helped ensure that long-running computations remained safeguarded against interruptions, which was crucial for working with extensive optimization models.

**Lessons Learned:**  
This project significantly enhanced my understanding of **linear programming**, **integer programming**, and **optimization techniques** in real-world applications. Additionally, it provided valuable hands-on experience in managing large datasets and implementing solutions with practical constraints, while reinforcing the importance of **checkpointing** to safeguard against data loss.
