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
- [ ] page that displays the tenants (tenant) current state
- [ ] component that displays the planned maintenance events

## How to do things

### Current stste of the system: 
-  poll the services for all tenants. List is from a config file. Can be hardcoded at 1st
-  if the service answers 200 then we consider it alive
-  we store the state in the database so that we can display it

### Prototype
![Image from iOS](https://user-images.githubusercontent.com/72201489/157202714-b3ca8627-b4f1-4b81-a24b-ccfc1fcbfd13.jpg)

### Planned maintenance
- list view of planned maintenance dates
- component for displaying data
- table in mongo that stores the planned maintenance events

### Business rules
1. Display the tenant status (tenant side):
```
Given that I am an user in Halden
When I enter the system 
Then I see Halden status
And I cannot see other tenants
```

2. Display all tenant status (visma side/ie role)
```
Given that I am an admin user
When I enter the system
Then I can see all tenants status
```

3. See the planned maintenance
```
Given that I am in the system
When I go to the status page
Then I can see the planned maintenance events
```

## Progress log
- 08:30 CET - Team gathering
- 08:45 CET - Learning and exploring existing solutions
- 10:00 CET - Start implementation
- 10:30 CET - Figma prototyping
- 11:00 CET - 1st code written
- 14:20 CET - Figma to HTML Export
- 15:30 CET - Break layout into Svelte components
![Real deal](/doc/img/img_01.png)
- 16:15 CET - Final discussions on linking with backend
- 12:15 CET - Nev version

![Retro](/doc/img/Screenshot%20from%202022-03-09%2015-51-03.png)

## Retrospective

![Retro](/doc/img/Screenshot%20from%202022-03-09%2015-45-32.png)


### Liked
* Nice to build something from scratch (2)
* Nice to spend time with collageus you dont work so much with (2)
* To team up with ppl with different roles to get to a result (1)
* Small team - easier to communicate (2)
* Nice to see things "live" and be able to give continuous feedback, also learn something new (1)

### Learnt
* Figma to HTML (1)
* Learned more about exporting Figma design directly to code (1)

### Lacked
* Better organization of the event
* Everybody in the same room (2)
* That we are not working more like this in real life

