# liri-node-app
For UW Coding Bootcamp 10-Week Homework (LIRI Bot)
Lead Developer:  Candice Chin
https://candicechin.com

## Technologies Used
JavaScript, node.JS, NPM packages, Bands in Town Artist Events API, Spotify API, IMDB API, Axios, Moment, and DotEnv

## Problem that LIRI Bot is Trying to Solve
LIRI Bot enables a user to use the command line to retrieve Bands in Town events, Spotiy, and Movie info in an organized and easy-to-read format. LIRI is like iPhone's SIRI, however while SIRI is a 
Speech Interpretation and Recognition Interface, LIRI is a 
Language Interpretation and Recognition Interface.  LIRI is a command line node app
that takes in parameters and gives back data to the user.

## Overview of App Organization
liri.js can take in one of the following commands:

concert-this
This will search the Bands in Town Artist Events API for an artist and render the following information about each event to the terminal:
   Name of the venue
   Venue location
   Date of the Event (use moment to format this as "MM/DD/YYYY")

![Concert-this](/images/concert-this.png)

spotify-this-song
This will show the following information about the song in your terminal/bash window
   Artist(s)
   The song's name
   A preview link of the song from Spotify
   The album that the song is from

![Spotify-this-song](/images/spotify-this-song.png)

movie-this
This will output the following information to your terminal/bash window:
   Title of the movie.
   Year the movie came out.
   IMDB Rating of the movie.
   Rotten Tomatoes Rating of the movie.
   Country where the movie was produced.
   Language of the movie.
   Plot of the movie.
   Actors in the movie.

![Movie-this](/images/movie-this.png)

do-what-it-says
   LIRI will use the text from “random.txt” and call on of LIRI’s commands. It should run Spotify-this-song for “I want it That way”.

![Do-what-it-says](/images/do-what-it-says.png)

## What Each Command Should Do

node liri.js concert-this <artist/band name here>

This will search the Bands in Town Artist Events API ("https://rest.bandsintown.com/artists/" + artist + "/events?app_id=codingbootcamp") for an artist and render the following information about each event to the terminal:

Name of the venue
Venue location
Date of the Event (use moment to format this as "MM/DD/YYYY")

node liri.js spotify-this-song '<song name here>'

This will show the following information about the song in your terminal/bash window

Artist(s)
The song's name
A preview link of the song from Spotify
The album that the song is from

If no song is provided then your program will default to "The Sign" by Ace of Base.
You will utilize the node-spotify-api package in order to retrieve song information from the Spotify API.
The Spotify API requires you sign up as a developer to generate the necessary credentials. You can follow these steps in order to generate a client id and client secret:

Step One: Visit https://developer.spotify.com/my-applications/#!/

Step Two: Either login to your existing Spotify account or create a new one (a free account is fine) and log in.

Step Three: Once logged in, navigate to https://developer.spotify.com/my-applications/#!/applications/create to register a new application to be used with the Spotify API. You can fill in whatever you'd like for these fields. When finished, click the "complete" button.

Step Four: On the next screen, scroll down to where you see your client id and client secret. Copy these values down somewhere, you'll need them to use the Spotify API and the node-spotify-api package.

node liri.js movie-this '<movie name here>'

This will output the following information to your terminal/bash window:

   * Title of the movie.
   * Year the movie came out.
   * IMDB Rating of the movie.
   * Rotten Tomatoes Rating of the movie.
   * Country where the movie was produced.
   * Language of the movie.
   * Plot of the movie.
   * Actors in the movie.

If the user doesn't type a movie in, the program will output data for the movie 'Mr. Nobody.'

You'll use the axios package to retrieve data from the OMDB API. Like all of the in-class activities, the OMDB API requires an API key. You may use trilogy.

node liri.js do-what-it-says
Using the fs Node package, LIRI will take the text inside of random.txt and then use it to call one of LIRI's commands.

It should run spotify-this-song for "I Want it That Way," as follows the text in random.txt.
Edit the text in random.txt to test out the feature for movie-this and concert-this.

## Instructions for running the App
Open Terminal Command Line, and use the node.js command for the following:
concert-this
spotify-this-song
movie-this
do-what-it-says

## Link to Deployed Version of App
https://github.com/cchin1/liri-node-app

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.