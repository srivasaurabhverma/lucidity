# Delivery Management System

## Overview

The Delivery Management System is a Java-based software solution designed to streamline the process of delivering orders from restaurants to customers by a delivery person. It employs various algorithms to generate optimal delivery routes and calculates the shortest delivery time, considering travel time between locations and food preparation time at restaurants.

## Flow

1. **Data Initialization**:
    - Initialize delivery persons, restaurants, and customers with their respective locations and attributes using the `initDeliveryPerson`, `initRestaurant`, and `initCustomers` methods in the `Main` class.

2. **Route Generation**:
    - The `RouteGenerator` class generates all possible routes starting from the delivery person's location, passing through restaurants, and ending at customers' locations.

3. **Route Filtering**:
    - The generated routes are filtered to ensure that each route starts from the delivery person's location, visits the correct restaurant before delivering to the corresponding customer, and follows a valid sequence of locations.

4. **Shortest Delivery Time Calculation**:
    - The `ShortestDeliveryTimeCalculator` class calculates the shortest delivery time among the filtered routes, taking into account travel time between locations and food preparation time at restaurants.

5. **Output**:
    - The shortest delivery time is displayed as output, providing an estimate of the time required to deliver the batch of orders.

## Features

- Automatic generation of delivery routes.
- Calculation of the shortest delivery time.
- Customizable food preparation time at restaurants.
- Efficient data management using maps.
- Object-oriented design for modularity and extensibility.

## Assumptions

- Each location on the map can have either one restaurant or one customer. There are no locations with both a restaurant and a customer simultaneously.
- The delivery person only goes to the customer's location to deliver the order after picking it up from the restaurant. There are no direct deliveries from the restaurant to the customer without the involvement of the delivery person.

## Usage

1. **Prerequisites**:
    - Java Development Kit (JDK) installed on your system.
    - Maven build tool installed.
   ``` bash
       sudo apt install maven
   ```

2. **Setup**:
    - Clone the project repository to your local machine.
    - Import the project into your preferred IDE.

3. **Configuration**:
    - Modify the initialization methods (`initDeliveryPerson`, `initRestaurant`, `initCustomers`) in the `Main` class to set up delivery persons, restaurants, and customers according to your requirements.

4. **Execution**:
    - Run the `Main` class to initialize data, generate routes, and calculate the shortest delivery time.

5. **Testing**:
    - Run the unit tests using the following Maven command:
      ```bash
      mvn test
      ```

6. **Customization**:
    - Adjust the food preparation time (`pt1` and `pt2` variables) in the `Main` class to reflect actual preparation times at restaurants.
