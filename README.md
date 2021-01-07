# Webizing Thing Description

The current repository is part of the TD project and represents the server side. The server part consists of: GraphQL API for obtaining the current state of the sensor, REST API represents a digital representation of the sensor in JSON-LD format, the database in which data about the current state of the sensor is stored. 
Each branch in the repository represents implementations of this project using different technologies for storing data(e.g. IPFS, OrbitDB, Textile, MongoDB) and the use of different sensors (e.g. Apple Watch, Smappee, Foobot)

Some sensors, such as Smappee and Foobot, store data in the clouds, so the server synchronizes the data received from the cloud with one of the databases used in this project.

In order to receive data from the apple watch, we use a mobile application that synchronizes the IOS health application with the server.

# Branches

Each branch represents a different implementation of a TD server using a different number of sensors and different technologies

schema-iot - store data in mongodb

k-log-textile - store data in textile db

me-centric - this branch part of the blockchain project, data stored in IPFS

ipfs - store data in ipfs

# Architecture


In the image below you can see the architecture of k-log-textile

![alt text](https://github.com/alexander-lipnitskiy/webizing-td/blob/master/textile-db-arch.png)

# Requirements
node.js - 12+

yarn - 1.19.1+

mongodb - 4.0

go-ipfs - 0.6.0+


# Installation 

Clone the repository data to your Operating System.

Use the package manager yarn to install modules.

```bash
yarn install
```

# Development

```bash
yarn run dev:start
```

# Production

```bash
yarn run dev:start
```

# Access API

By default the server runs on port 4000.

Example of GraphQL request http://localhost:4000/graphql

![alt text](https://github.com/alexander-lipnitskiy/webizing-td/blob/master/graph-ql.png)


Rest API root request http://localhost:4000/td

Example of Rest API request to the air quality sensor http://localhost:4000/td/airquality

![alt text](https://github.com/alexander-lipnitskiy/webizing-td/blob/master/rest-api-td.png)
