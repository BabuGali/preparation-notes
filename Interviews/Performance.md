- In Java, performance can be affected by a variety of factors, including the code itself, the JVM implementation, and the hardware it runs on.
- Common performance bottlenecks include inefficient algorithms, excessive memory usage, excessive CPU usage, and I/O operations.
-  5 Common Java Performance Problems
	- Memory Leaks and Out of Memory Errors
	- Thread Deadlocks
	- Garbage Collection
	- Code-Level Issues
	- Pool Connections
 - Optimizing performance can improve user experience, reduce hardware requirements, and increase the overall productivity and profitability of an application.
 - some basic parameters that can be tuned to improve Java performance include:
	 - **Footprint**- Tuning the footprint involves minimizing the amount of memory and CPU resources used by the application
	 - **Throughput** - The amount of work that can be performed by a Java application within a given period of time
	 - **Latency** - The time it takes for a Java application to respond to user requests
	 - However, these parameters are interrelated, and tuning one parameter may affect the others. For example, combining low memory usage with high throughput increases latency. Therefore, it is important to prioritize and balance the parameters based on the specific requirements of the application and the available resources.
- Java Profile
	- A Java profiler is a tool that can assist in identifying performance bottlenecks in a Java application. Most bottlenecks result from the limitations of major shared resources, such as memory, CPU, input/output operations, and threads.
- Create performance test suite
- ## 8 Tips for Optimizing and Improving Java Performance
	- **Avoid Writing Long Methods
	- **Use PreparedStatement instead of Statement
	- **Use Caching
	- **Use Stored Procedures/views Instead of Queries
	- **Leverage StringBuilder
	- **Optimize If-Else Statements
	- **Don’t Over-optimize
	- **Use Java Profilers
	- **release DB connections
	-  **Avoid Getting the Size of the Collection in the Loop
	- **Avoid Using String Objects For Concatenation
	- **Avoid Creating Big Objects Often
	- **Use of Unnecessary Log Statements and Incorrect Log Levels
	- **Monitor and Analyse
	-  **fetch the Data Using Joins
	- **Use Primitive Types Wherever Possible
		-  You can also use primitive types in your applications to reduce processing overhead and increase performance. It’s better to use an **int** instead of an **Integer**, or a **double** instead of a **Double**. While primitive types are stored in the stack, instances of classes, (i.e., objects), are stored in the garbage collected heap.
		- Using this method, your application’s performance can improve considerably, since the stack is faster than the heap with much less resource overhead.
	 - **Avoid Using Regular Expressions in Your Java Code