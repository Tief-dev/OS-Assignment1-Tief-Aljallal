# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

A process is an independent program in execution with its own memory space and system resources, while a thread is a smaller unit of execution within a process that shares the same memory with other threads. Threads are lighter and faster to create compared to processes, which makes them more efficient for handling multiple tasks concurrently. Processes require more overhead because each one needs its own memory and communication between them is more complex. In contrast, threads can communicate easily since they operate within the same memory space. In this assignment, threads were used instead of processes because they allow efficient simulation of multiple tasks without the heavy resource cost of creating separate processes. This makes the program faster and simpler while still demonstrating CPU scheduling behavior.

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

In Round-Robin scheduling, if a process does not finish within its allocated time quantum, it is paused and placed back at the end of the ready queue. This allows other processes to use the CPU, ensuring fairness among all processes. The process will then wait for its turn again and continue execution in the next cycle. This behavior repeats until the process completes its execution. This approach prevents any single process from monopolizing the CPU and ensures that all processes get equal opportunity to run.

Example from my output:
```
P1 (Priority: 3) starts execution
P1 did not finish, remaining time: 2000ms
P1 is re-added to the ready queue

P2 (Priority: 4) starts execution
```

**Explanation of example:**
In this example, process P1 starts execution but does not complete within its time quantum. As a result, it is paused and re-added to the end of the ready queue with its remaining execution time. After that, the scheduler selects the next process, P2, to run. This demonstrates how Round-Robin scheduling ensures fairness by allowing each process to take turns using the CPU instead of letting one process run continuously until completion.

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

New:
P1 is in the New state when its thread is first created using new Thread(process). At this point, the thread object exists but has not started executing yet. This happens when the process is added to the ready queue but before start() is called.
Runnable:
P1 moves to the Runnable state when currentThread.start() is called. In this state, the thread is ready to run and waiting for the CPU scheduler to select it. It is placed in the ready queue along with other processes and will run when it gets its turn.
Running:
P1 enters the Running state when the CPU scheduler selects it and its run() method starts executing. During this time, the process uses the CPU for its assigned time quantum or until it finishes execution. This is where the actual processing happens.
Waiting:
P1 enters the Waiting state when the main thread calls currentThread.join(). This causes the main thread to wait until P1 finishes its current execution. Additionally, if the process does not complete within its time quantum, it may also effectively wait in the ready queue before getting CPU time again.
Terminated:
P1 reaches the Terminated state when its execution is complete and its remaining time becomes zero. At this point, the thread finishes execution and is no longer scheduled again. The process is removed from the system and does not return to the ready queue.

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: Web Server Handling Multiple Client Requests

Description:
A web server often needs to handle requests from many users at the same time. Each user request (such as loading a webpage or submitting a form) can be handled by a separate thread. These threads are managed concurrently to ensure that multiple users are served without delay.

Why Round-Robin works well here:
Round-Robin scheduling ensures that each request gets a fair share of CPU time, preventing any single request from blocking others. This improves responsiveness, especially when many users are accessing the server simultaneously. It also provides predictable performance because each thread gets a fixed time slice. This helps maintain smooth and balanced handling of multiple client requests.

### Example 2: Interactive Applications (e.g., Games or GUI Applications)

Description:
Interactive applications such as games or graphical user interface (GUI) programs often perform multiple tasks at once, such as rendering graphics, processing user input, and handling background computations. These tasks can run on separate threads to improve performance and user experience.

Why Round-Robin works well here:
Round-Robin scheduling ensures that each task gets CPU time regularly, preventing any single task from dominating the system. This is important for maintaining responsiveness, such as ensuring that user input is processed quickly while other tasks continue running. It also provides fairness among tasks and keeps the application running smoothly. The predictable time-sharing makes it suitable for real-time interaction.

---

## Summary

Key concepts I understood through these questions:

The difference between threads and processes, especially how threads share memory and are more efficient for concurrent execution.
How Round-Robin scheduling works, including how processes are re-queued and given equal CPU time for fairness.
The lifecycle of a thread and how it transitions between states like New, Runnable, Running, Waiting, and Terminated during execution.

Concepts I need to study more:

Advanced thread synchronization and how threads communicate safely in more complex systems.
Detailed CPU scheduling algorithms beyond Round-Robin, such as priority scheduling and shortest job first.
