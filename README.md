# Random-User-API-Performance-Test

This project involves performing a load test on the URL `https://random-data-api.com/api/v2/users` to determine the actual transactions per second (TPS) for 120,000 users over 12 hours. The project also identifies the system's bottleneck/stress test point and capacity TPS. The results are documented in Excel sheets and visualized through screenshots.

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

### Repository Structure

- **README.md:** This file.
- **test-plan.jmx:** JMeter test plan file.
- **resources:** Folder containing Excel files with test reports.
- **screenshots:** Folder containing screenshots of the reports.

### Cloning the Repository

1. Clone or download the project repository:

```bash
git clone https://github.com/your-username/Random-User-API-Performance-Test.git.```

