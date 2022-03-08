# Hackathon 2022

## Problem statement

![Looking at the same thing](https://www.sloww.co/wp-content/uploads/2020/08/The-Blind-Men-and-the-Elephant.png)

What is bringing value to the user?
- get an overview of planned mainenance in the future
- state of the services and a cause for it
- detailed look on each service
- when the client gets a call they need to get a page where to look for the issues
- APIs, integrations state
- overview of the total state
- possibility of the drill-down
- current state of the system and planned maintenance
- historical state of the system

Most important:
- current state of the system
- planned maintenance announcements
![Current state](https://wac-cdn.atlassian.com/dam/jcr:fb5dbd0c-a8a8-4f70-b68b-87504511ca6c/dropbox-nodropshadow.png?cdnVersion=245)

## Deliverables

## How to do things

### Current stste of the system: 
-  poll the services for all tenants. List is from a config file. Can be hardcoded at 1st
-  if the service answers 200 then we consider it alive
-  we store the state in the database so that we can display it

### Planned maintenance
- list view of planned maintenance dates
- component for displaying data
- table in mongo that stores the planned maintenance events

