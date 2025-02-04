# Project-4
Sprint 5 Project 5

Sprint 5: Understanding Databases


# Project Task
This project consists of two parts, which both require you to use the console to access a remote server. In the first part, you'll work with files and directories and then in the second part, you'll work with the database of a taxi service. 

# Task 1
The developers have sent a task: we need to determine which requests came from a particular IP address. The IP address consists of four numbers separated by dots. You need addresses that start with "233.201."

The logs are stored on a remote server in /logs/2019/12 but we don't know which day the error occurred.

Your task is to find the requests that were sent.

# Please include the following in your answer:

The command to get you the necessary logs
The results of your search, in the form of logs (e.g., 233.201.31.161 - - [30/12/2019:21:38:13 +0000] "PUT /alerts HTTP/1.1" 400 3557)
-------------------------------------------------------------------------------------------------------------------------------------

# Task 2
A bug was detected in the system. It appeared twice: first on 30.12.2019 and then again on 31.12.2019. The developers want to investigate the bug by examining logs that contain 400 and 500 error codes. For now, they only want to focus on the first day. 

Your task is to find the logs from the first day and save them in a single file. Then, you need to split the results into two separate files, based on the error code.

# Follow these steps to complete the task:

1. Сreate a directory in the home directory on the remote server called "bug1."
2. Put all requests that occurred during the specified period in the main.txt file in the /bug1 directory.
3. Create an events directory, called "events," inside the /bug1 directory.
4. Create files for the error codes inside the /events directory. Name these files 400.txt and 500.txt, respectively, and place the logs from the main.txt file into the corresponding file.
   
# Please include the following in your answer:

The commands you used to create the /bug1 and /events directories.
The commands you used to select logs for the specified periods (these are the requests that you use to select logs for the main.txt file).
The commands you used to put logs from the main.txt file into the 400.txt and 500.txt files.
The results of your work (i.e., the contents of 400.txt and 500.txt). Since there will be many lines of text, you'll provide a selection of the output, as below: 1. The line count of 400.txt. Use wc ~/bug1/events/400.txt to get the answer. 2. The first 3 lines from 400.txt. Use head -3 ~/bug1/events/400.txt to get the answer. 3. The last 3 lines from 400.txt. Use tail -3 ~/bug1/events/400.txt to get the answer. 4. The line count of 500.txt. Use wc ~/bug1/events/500.txt to get the answer. 5. The first 3 lines from 500.txt. Use head -3 ~/bug1/events/500.txt to get the answer. 6. The last 3 lines from 500.txt. Use tail -3 ~/bug1/events/500.txt to get the answer.
Databases
# Data Description
Database of taxi rides in Chicago:

The neighborhoods table contains information about parts of the city:

neighborhood_id — neighborhood code
name — neighborhood name
The cabs table contains information about taxis:

cab_id — unique car code
vehicle_id — technical identifier of the vehicle
company_name — name of the cab company
The trips table stores information about rides:

trip_id — trip code
cab_id — code of the car for the trip
start_ts — date and time of the start of the trip (time rounded up to the nearest hour)
end_ts — date and time of the end of the trip (time rounded up to the nearest hour)
duration_seconds — duration of the trip in seconds
distance_miles — distance of the trip in miles
pickup_location_id — code of the neighborhood where the trip started
dropoff_location_id — code of the neighborhood where the trip ended
The weather_records table contains information about the weather:

record_id — code for a weather observation record
ts — date and time of the observation (time rounded up to the nearest hour)
temperature — temperature at the time of observation
description — brief description of the weather conditions (for example, "light rain" or "scattered clouds")
------------------------------------------------------------------------------------------------------------


# Task 3
You have a database with taxi rides. According to the plan, a total of 10,550 cars were supposed to enter the service line, which should have covered the user demand. However, the team received many complaints that there were not enough available cars. How many taxis actually entered the line? The cabs table contains information about the entire taxi pool.

1. Log in to the remote server.
2. Connect to the chicago_taxi database using the login morty and password smith.
3. Calculate the total number of cars in the cabs table. Keep in mind that one car may belong to multiple companies.
Please include the following in your answer:

The number of cars
The query that you used to solve this task
--------------------------------------------------------------------------------------------------------------------------------------------
# Task 4
Calculate the number of cars for each company in the cabs table. Sort the values in descending order. The team suggests that some companies have not put enough cars on the line.

Extract companies with fewer than 100 cars. Name the field with the number of cars cnt, and the field with the company name company_name.

To solve the problem, use the HAVING operator, which is an analog of WHERE for aggregate functions. Study this documentation to learn how the operator works:

Please include the following in your answer:

A list of companies with fewer than 100 cars
The query that you used to produce the list above
Please note that the complete list may not be displayed in the console. 




