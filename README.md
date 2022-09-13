# Vendee Globe Business Case

![Vendee Globe Image](https://github.com/GrainneKennedy/VendeeGlobeBusinessCase/blob/main/Intro2.png?raw=true)

## Welcome to Vendee Globe Business Case

The Vendée Globe is a solo non-stop round the world yacht
race founded by Philippe Jeantot in 1989. The race takes place
every four years and is considered an extreme quest of
individual endurance and the ultimate test in ocean racing.
The 9th edition of the Vendee Globe was held in 2020-2021
and was won by French sailor Yannick Bestaven who took
slightly over 80 days to sail non-stop around the globe.
During the race, spectators could follow the action live on an
online racing dashboard. The technology for tracking the boats
live was provided by Nokia.

## Your challenge

In this business case, you will assume the role of Nokia. You will build a cloud-based [Lambda Architecture](https://en.wikipedia.org/wiki/Lambda_architecture) to process the telemetry data from the sailing boats. Your architecture should run in Azure and contain a real-time path for processing sailing boat data in real time, and a batch-processing path for collecting sailing boat data in batches and performing calculations on those batches. 

![Lambda Architecture](https://github.com/GrainneKennedy/VendeeGlobeBusinessCase/blob/main/lambda_architecture.png?raw=true)

The Lambda Architecture should send all boat data to a PowerBI dashboard. The dashboard should display a world map with the current position of each boat, and a table with a ranking of racing teams. The ranking table should be sorted by who is currently in the lead. 

We are currently between races, so unfortunately we cannot use the actual data from the boats participating in the race. Instead, you are going to use a [Python application](./race_simulator.py) that will simulate boat telemetry data from a fleet of 10 race participants. 

To complete this business case, you will need to do the following:

1. Create a Lambda Architecture in Azure with a real-time path and a batch-processing path. Your architecture should include an Event Hub, a Stream Analytics Job, and an output to PowerBI. Your batch-processing path can use any data storage service you prefer: a Data Lake, a SQL Database, a Cosmos database, or a Synapse Analytics Workspace.
2. Create a PowerBI dashboard that displays a world map with the current location of each racing team, and a table with the teams ranked by position in the race.
3. Download the Python race simulation app to your local computer. Configure the app to send data to your EventHub.
4. Start the Python app. Every 60 seconds, the telemetry of the simulated racing boats will be sent to your Azure cloud.

You will have completed the business case if your PowerBI dashboard correctly shows the position and ranking of each sailing team in the race.

Good luck!

## Getting started

To help us get started, guided instructions were given to build the first piece of the Lambda Architecture which consisted of an Event Hub and instructions to get the Python sailing simulator up and running. 

To complete the business case, here's what we needed to add:

* The remaining pieces of the Lambda Architecture: a Stream Analytics Job, an output to PowerBI, and a second output to a data storage service of our choice.
* A data storage service of our choice to store batch data: a Data Lake, a SQL Database, a Cosmos database, or a Synapse Analytics Workspace.
* A view or stored procedure or Synapse notebook to calculate the table of teams ranked by position in the race.
* A PowerBI dashboard that displays a world map with the current location of each racing team, and a table with the teams ranked by position in the race.

We will have completed the business case when our PowerBI dashboard correctly shows the position and ranking of each sailing team in the race. 

## Challenges

During the business case, we will need to address several challenges:

* The Python app occasionally produces garbled data. We need to ensure that only clean data arrives in the PowerBI dashboard? 
* How are we going to calculate the ranked list of sailing teams? How will we calculate who is ahead in the race?
* Which data service are we going to use for the batch-processing path in the Lambda Architecture?
* How will we present our data in the PowerBI dashboard?

There are multiple solutions for each challenge but we will descirbe here the decisions we made to address each of these challenges and present our final solution

![Vendee Globe Image](https://github.com/GrainneKennedy/VendeeGlobeBusinessCase/blob/main/Intro2.png?raw=true)
 
![Intro](https://github.com/GrainneKennedy/VendeeGlobeBusinessCase/blob/main/intro.png?raw=true)

![Business Requirements](https://github.com/GrainneKennedy/VendeeGlobeBusinessCase/blob/main/requirements.png?raw=true)

![Challenges](https://github.com/GrainneKennedy/VendeeGlobeBusinessCase/blob/main/Challenges.png?raw=true)
![From Portugal](https://github.com/GrainneKennedy/VendeeGlobeBusinessCase/blob/main/from%portugal.png?raw=true)
![To Dashboard](https://github.com/GrainneKennedy/VendeeGlobeBusinessCase/blob/main/dashboard.png?raw=true)


