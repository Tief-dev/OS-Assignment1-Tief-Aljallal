# Reflection Questions

## Instructions
Answer the following questions about your learning experience. Each answer should be **at least 5-7 sentences** and show your understanding.

---

## Question 1: What did you learn about multithreading?

Through this assignment, I gained a deeper understanding of how multithreading works in Java, particularly how threads allow multiple processes to be executed concurrently within a single program. I learned how threads are created using the Runnable interface and executed using the Thread class. Additionally, I understood how thread scheduling works in a Round Robin system, where each process is given a fixed time quantum. This helped me see how fairness is maintained among processes and how context switching occurs between them. I also learned how threads can be synchronized using methods like join() to control execution flow. Overall, this assignment helped me connect theoretical concepts of multithreading to practical implementation.

---

## Question 2: What was the most challenging part of this assignment?

The most challenging part of this assignment was implementing the waiting time tracking feature. It required careful tracking of when a process enters the ready queue and when it starts executing. Initially, I struggled with determining the correct placement of the time calculation logic. There were also issues with variable naming and ensuring consistency across the class, which led to compilation errors. Another challenge was understanding how the same process could re-enter the queue multiple times in a Round Robin system. This made it necessary to accumulate waiting time correctly rather than overwrite it. Overall, the difficulty came from both logic placement and debugging small syntax errors.

---

## Question 3: How did you overcome the challenges you faced?

I overcame these challenges by carefully analyzing the program flow and identifying key points where processes change state. I focused on understanding when a process enters the queue and when it begins execution, which helped me correctly calculate waiting time. I also used debugging techniques such as reading error messages and checking variable names to fix syntax issues. Breaking the problem into smaller steps made it easier to manage and implement each feature individually. Additionally, testing the program after each change helped me verify correctness and catch errors early. This step-by-step approach made the overall implementation much more manageable.
---

## Question 4: How can you apply multithreading concepts in real-world applications?

Multithreading is widely used in real-world applications to improve performance and responsiveness. For example, web servers use multithreading to handle multiple client requests simultaneously without blocking other users. In user interface applications, multithreading allows background tasks to run without freezing the main interface, improving user experience. It is also used in gaming, where different threads can handle rendering, physics, and user input at the same time. Additionally, operating systems rely heavily on multithreading for process scheduling and resource management. Overall, multithreading enables efficient use of system resources and enhances application performance.

---

## Additional Reflections (Optional)

### What would you like to learn more about?

[Any topics related to threading, concurrency, or operating systems that you're curious about?]

---

### How confident do you feel about multithreading concepts now?

[Rate yourself and explain: Beginner / Intermediate / Confident]

[Explain your rating - what do you understand well? What needs more practice?]

---

### Feedback on the assignment

[Any comments about the assignment? Was it helpful? Too easy/hard? Suggestions for improvement?]
