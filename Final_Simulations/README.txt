Name: Jaswinder Singh
Studnet ID: x19219997 (Cohort 'A')
Module: Modelling, Simulation and Optimization (CA-1)
CA Task 1: Simulation of a two lane motorway and calculation of throughput, average travelling time, average speed and traffic density

Details: The first task involves simulating a two lane motorway and then calculating the below mentioned quantities. For accomplishing this task, we have used the code provided in the class and added the following components to it:

1. chooseLane() method: This function allows a vehicle to choose between the two lanes at random but with specific weights given to each lane. For the left/slow lane, we have given a weight of 0.80 since majority of the vehicles will be starting from this lane only. The right/fast lane is given a weight of 0.20 since only a small fraction of incoming vehicles pass through this lane.
2. We have used different inter-arrival times for each of the two lanes IAT_fast and IAT_slow. We ran different simulations with different values for the two inter-arrival times.
3. A condition is added to the main simulation loop allowing vehicles starting from the left lane to use IAT_fast and those starting from the right lane to use \textit{IAT_slow}.
4. For calculating the iat, a uniform distribution has been used instead of an expovariate distribution to reduce the variation. Moreover, expovariate distribution generated a few extremely small values like 0.0048 for the inter-arrival time which caused crashes.

The following four quantities have been computed from the simulation dataframe.

1. Throughput: Cumulative volume across all the lanes going in one direction measured and averaged over a prolonged period of time.
2. Average Travelling time: Average time taken by a vehicle to cross the entire motorway.
3. Average Speed:  Length of the motorway/Average travelling time 
4. Traffic density:  Throughput/Average speed

CA Task 2: Simulation of a two lane motorway incorporating the human driving behaviour.

Details: The second task is an extension of the first task to simulate the human driving behaviour. In this task, we will be using the freeMotorwaySpeed() function from the trafffic data generation file for generating the speed of the vehicles. Another aspect introduced to capture the real world scenario is the use of chooseVehicle() method which randomly generates a vehicle type between electrical and diesel for the simulation. The minimum and maximum accelerations will be decided for the vehicle based on the choice generated(electrical or diesel).

## The entire code file can be run in one go. There are no additional data files. Everything that is required is present within the code itself.