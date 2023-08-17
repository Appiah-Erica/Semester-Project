# Semester-Project 16

Name: Appiah Erica

Index Number: UEB3259722

Project Description;

This C++ code simulates the behavior of a basic traffic light using multi-threading. Let's break down the code step by step:

The code includes necessary header files for input/output (<iostream>), threading (<thread>), and time manipulation (<chrono>).

An enumeration TrafficLightColor is defined using the enum class construct. It contains three values: RED, GREEN, and YELLOW. This enum is used to represent the different states of the traffic light.

A class TrafficLight is defined to encapsulate the functionality of the traffic light. It has the following public methods:

TrafficLight(): This is the constructor of the TrafficLight class. It initializes the current traffic light color to RED.

start(): This method is used to start the traffic light simulation. It sets the isRunning flag to true and creates a new thread (controlThread) that will execute the controlLoop method.

stop(): This method is used to stop the traffic light simulation. It sets the isRunning flag to false and waits for the controlThread to finish using the join method.

The private member functions of the TrafficLight class are as follows:

controlLoop(): This method represents the core logic of the traffic light simulation. It runs in a loop while isRunning is true. Inside the loop, it uses a switch statement to handle the different traffic light colors. It prints the corresponding color and then waits for a specific duration using the std::this_thread::sleep_for function. After each sleep, the color is updated to the next state in the sequence (RED -> GREEN -> YELLOW -> RED).

The private member variables include currentColor to track the current color of the traffic light, isRunning to control the simulation loop, and controlThread to hold the thread that runs the controlLoop.

In the main function:

An instance of the TrafficLight class named trafficLight is created.

The start method of trafficLight is called, initiating the traffic light simulation in a separate thread.

The program then sleeps for 30 seconds using std::this_thread::sleep_for to simulate the traffic light simulation running for a while.

Finally, the stop method is called on the trafficLight instance to end the simulation. The program returns 0 to indicate successful execution.

In summary, this code demonstrates a basic traffic light simulation using C++ threads. It showcases how multi-threading can be used to control the behavior of the traffic light, allowing it to change colors and simulate a simple traffic light cycle.




