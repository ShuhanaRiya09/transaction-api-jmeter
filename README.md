# JMeter Performance Testing Project

## Project Overview
This project involves creating a JMX file for Apache JMeter to automate a series of positive test cases based on the following scenario:

1. Admin creates an agent and a customer.
2. Deposit 2000 TK to the agent from the system account.
3. Deposit 1000 TK to the customer from the agent account.
4. Check balance from the customer account.
5. Withdraw 500 TK from the customer account.
6. Payment of 200 TK from the customer account to a merchant.

The objective is to simulate these actions and measure the performance of the system under test.

## Prerequisites
- Java (JDK 8 or above)
- Apache JMeter (version 5.0 or above)

## Installation
1. **Install Java**: Ensure that you have JDK 8 or above installed on your system. You can download it from the [official Oracle website](https://www.oracle.com/java/technologies/javase-downloads.html).
2. **Download JMeter**: Download the latest version of Apache JMeter from the [official JMeter website](https://jmeter.apache.org/download_jmeter.cgi).
3. **Extract JMeter**: Extract the downloaded JMeter archive to a desired location on your computer.

## Creating the JMX File
Follow the steps below to create the JMX file for the given scenario:

1. **Open JMeter**: Navigate to the `bin` directory of your JMeter installation and run `jmeter.bat` (Windows) or `jmeter.sh` (Mac/Linux).

2. **Create a Test Plan**:
   - Open JMeter and create a new test plan.
   - Right-click on the Test Plan and add a Thread Group: `Add > Threads (Users) > Thread Group`.
   - Set the number of threads (users), ramp-up period, and loop count as needed.

3. **Add HTTP Request Defaults**:
   - Right-click on the Thread Group: `Add > Config Element > HTTP Request Defaults`.
   - Configure the server name or IP, and port number of the system under test.

4. **Add HTTP Requests**:
   - **Create Agent and Customer**: Add an HTTP Request sampler for the admin to create an agent and a customer.
     - Method: `POST`
     - Path: `/createUser`
     - Parameters: `{ "role": "agent" }` and `{ "role": "customer" }`
   - **Deposit to Agent**: Add an HTTP Request sampler to deposit 2000 TK to the agent from the system account.
     - Method: `POST`
     - Path: `/transacton/deposit`
     - Parameters: `{ "fromAc": "SYSTEM", "toAc": "agent", "amount": 2000 }`
   - **Deposit to Customer**: Add an HTTP Request sampler to deposit 1000 TK to the customer from the agent account.
     - Method: `POST`
     - Path: `/transacton/deposit`
     - Parameters: `{ "fromAc": "agent", "toAc": "customer", "amount": 1000 }`
   - **Check Balance**: Add an HTTP Request sampler to check the balance from the customer account.
     - Method: `GET`
     - Path: `/transacton/balance`
     - Parameters: `{ "ac": "customer" }`
   - **Withdraw**: Add an HTTP Request sampler to withdraw 500 TK from the customer account.
     - Method: `POST`
     - Path: `/transacton/withdraw`
     - Parameters: `{ "fromAc": "customer", "amount": 500 }`
   - **Payment**: Add an HTTP Request sampler for the payment of 200 TK from the customer account to a merchant.
     - Method: `POST`
     - Path: `/transacton/payment`
     - Parameters: `{ "fromAc": "customer", "toAc": "merchant", "amount": 200 }`

5. **Add Listeners**:
   - Right-click on the Thread Group: `Add > Listener > View Results Tree`.
   - Right-click on the Thread Group: `Add > Listener > Summary Report`.

6. **Save the Test Plan**: Save the test plan as `scenario.jmx`.

## Running the Test Plan
1. Open JMeter.
2. Load the `scenario.jmx` file.
3. Run the test by clicking on the green start button.
4. Monitor the test results in the listeners.

## Conclusion
This project provides a structured way to automate and measure the performance of a system based on a specified scenario using Apache JMeter. Follow the steps outlined above to create and execute your JMX test plan.
