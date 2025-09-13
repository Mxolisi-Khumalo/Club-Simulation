# Club Simulation – Concurrency in Action  
*A concurrency-driven simulation of a nightclub environment using Java*  

---

## About the Project  

The **Club Simulation** is a Java program that models a real-life nightclub environment while showcasing the use of **concurrency and synchronization techniques**. Think of it as a virtual club where patrons (clubgoers) enter, enjoy themselves, and leave — all while the program ensures no chaos occurs at the doors or on the dance floor.  

This project was built as part of a **Concurrency Assignment (2023)** to demonstrate:  
- Thread safety  
- Deadlock prevention  
- Synchronization techniques  
- Real-world concurrency concepts in a fun and interactive way  

---

## Features  

✅ **Realistic Patron Behavior** – Clubgoers queue outside if the venue is full and enter only when space frees up.  
✅ **Limited Capacity** – Inside the club, the number of people never exceeds the set maximum.  
✅ **Activities & Movement** – Patrons can:  
- Get drinks at the bar 
- Wander around the club 
- Dance on the floor 

✅ **Fair & Safe Simulation**  
- Only one person can enter/exit at a time 
- Patrons keep safe “distance” from each other on a grid 
- Strict deadlock prevention & synchronized movement  

✅ **Interactive Controls**  
- **Start Button** – Launch the simulation  
- **Pause/Resume Button** – Freeze and continue activity safely  
- **Quit Button** – End the program gracefully  

---

## Usage  

### Prerequisites  
- Java 8+ installed on your system  
- `make` installed (for running via Makefile)  

### Run the Simulation  
1. Clone this repository:  
   ```bash
   git clone https://github.com/USERNAME/Club-Simulation.git
   cd Club-Simulation
   ```
2. (Optional) Adjust command line inputs in the `run` method of the Makefile to customize your simulation.  
3. Start the simulation with:  
   ```bash
   make run
   ```
4. Use the buttons in the simulation window to manage the club:  
   - ▶️ **Start** – Begin the simulation  
   - ⏸️ **Pause/Resume** – Control flow without breaking the program  
   - ❌ **Quit** – End session  

---

## ⚙Technical Details  

This simulation demonstrates how concurrency is handled in Java using:  
- **Synchronization (`synchronized`, `wait()`, `notify()`)** – Prevents multiple patrons from entering the same door at once.  
- **Latches** – Ensures the simulation only starts when triggered by the user.  
- **Atomic Variables (`AtomicBoolean`)** – Used to safely pause/resume operations.  
- **Thread-Safe Movement Rules** – Patrons move step-by-step, avoiding overlap.  
- **Deadlock Prevention** – Ensures smooth flow so all threads eventually progress (no "frozen club").  

This setup models real concurrency challenges like **thread synchronization, fairness, and resource sharing**, which developers also face in fields like server design, distributed systems, and gaming.  

---

## Demo (Optional)  
👉 *(Add screenshots or a gif of the simulation running here!)*  

---

## Author  
- **Mxolisi Khumalo**  

> This project was created as an educational tool to explore concurrency fundamentals in a practical, engaging way.  

---

## Future Ideas  
Some potential improvements to make the club even more fun:  
- Support for multiple entrances & exits  
- Different patron behaviors/personalities  
- Dynamic club capacity that changes over time  
- Visualization improvements with animations  

---

## Contribute / Feedback  
If you'd like to improve this simulation, feel free to **fork** the repo, submit **pull requests**, or open **issues**. Suggestions are always welcome!  

---  

### Closing Note  
This project isn’t just about coding — it’s about showing how computing concepts like **threads, synchronization, and resource management** can be easily applied to real-world analogies. After all, managing a nightclub full of people isn’t too different from managing simultaneous users in a distributed system.
