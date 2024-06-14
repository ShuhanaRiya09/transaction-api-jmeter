# Random-User-API-Performance-Test

This project involves performing a load test on the URL https://swapi.dev/api/people/ to determine the actual transactions per second (TPS) for 120,000 users over 12 hours. The project also identifies the system's bottleneck/stress test point and capacity TPS. The results are documented in Excel sheets and visualized through screenshots.The Star Wars API (SWAPI) is a RESTful web service that provides access to various data related to the Star Wars universe. The API is designed to be a comprehensive and easy-to-use resource for developers who want to access information about characters, films, species, starships, vehicles, and planets from the Star Wars franchise.

Here is a breakdown of what the SWAPI provides, specifically for the endpoint https://swapi.dev/api/people/:

## Test Scenario

### Objectives

1. **Determine Actual TPS:**
   - Verify if the system can handle the expected TPS for 120,000 users over 12 hours.
   - Calculate the actual TPS.

2. **Identify Bottleneck/Stress Test Point:**
   - Find the point at which the system starts showing a 1% error rate.

3. **Determine Capacity TPS:**
   - Identify the maximum TPS the system can handle without errors.

## Requirements

- Apache JMeter installed on your machine
- Basic understanding of JMeter and performance testing
- A working instance of the Random User API

## Setup Instructions

### Apache JMeter Installation
1. Download and install Apache JMeter from the [official website](https://jmeter.apache.org/download_jmeter.cgi).


### Resources:

## Load Test and Stress Test reports in Excel format.
You can download the Excel files from the following links:
- [Load&stresstest.xlsx](https://docs.google.com/spreadsheets/d/1NQoul8f9fX15vutBTHN46yBVwDtDyF7A/edit?usp=sharing&ouid=106900521374584856661&rtpof=true&sd=true)

## Screetshot of Excel sheets:

## Load Test:

![Load](https://github.com/ShuhanaRiya09/Random-Covid-19-API-Performance-Test/assets/108625095/2e171cf0-e342-4fcc-bda0-6c8d3fa314c2)
## Stress Test:

![s](https://github.com/ShuhanaRiya09/Random-Covid-19-API-Performance-Test/assets/108625095/c5903eb9-7c26-42a1-baf4-d2cb342af1db)



## Outputs:

## Jmeter HTML Report:

![tttt](https://github.com/ShuhanaRiya09/transaction-api-jmeter/assets/108625095/45f2055c-46ef-42ef-b956-0d8e55d7adf9)



## Conclusion :
The performance testing of the Random User API demonstrated its ability to handle the expected load of 120,000 users over 12 hours. The Load Test confirmed the API meets the required TPS, while the Stress Test identified the bottleneck at which a 1% error rate occurs. These insights provide a foundation for future optimizations and scaling efforts, ensuring the API remains robust under increased loads.
