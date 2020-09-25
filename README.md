# SafeMaps
  SafeMaps is a platform that allows for people to make conscious decisions before leaving their homes. Using cameras running a person detection algorithm, data can be collected on how well social distancing is being practiced in the area. These cameras would be installed in public places like large couryards, parks, and other open spaces. The data is then sent back to a database in real time and rendered as a heat map for the end user, allowing them to plan an evening out, morning jog, or commute to work before even leaving home. 

## Technology Used
OpenCV and Python was used to process the video data. 
The front end for the website was created made with ReactJS. All of the data produced by the videos is stored on a postgres server and accessed via POST/GET requests served by a cherrypy server

## Installation/Running

To launch the website, go to `/web/ui` and run the following:
```
npm i
npm start
```
Doing so will launch the website on http://localhost:8080
If you'd like to run your own instance of the postgres db to connect to, go to `/web/server/ ` and copy `conf.default.json` into a file called `conf.json` After filling out the necessary fields run:

```
python3 postgres.py
python3 server.py
```
You will need a running postgres instance in order for this to work.

# Inspiration
Covid19 pandemic
Traffic maps used by news agencies.

# What it does
SafeMaps is a platform that consists of a network of cameras installed in public spaces like parks and busy streets. Using computer visions, these cameras allow us to count the number of social distancing violations (maintaining a 6 feet distance between people) in real-time and log them in a database. This data is then displayed by a website that a user could check before making plans to determine the best places to enjoy the outdoors while also reducing the risk of exposure to COVID.

# How we built it
We used OpenCV to process video inputs and send over the number of social distancing violations to a postgres db. This data is queried by the website and displayed to the user in a heatmap.

# Challenges we ran into
Accounting for camera perspective in distance calculations
Working with the google-maps-react API to get the heatmap displayed
Accomplishments that we're proud of
Successfully implementing human detection and perspective correction algorithm
Putting together a simple but effective UI that displays all of the data in real-time as its collected

