# Musical Odyssey
HackSheffield 10 submission for the theme **Odyssey**, written in Java and Spring Web.

Uses:
- OpenStreetMaps
- Nominatim
- Spotify API
- LastFM API

You will require API keys for LastFM and Spotify.

## Screenshots

<img width="1264" height="577" alt="eg1" src="https://github.com/user-attachments/assets/d642e75e-cb16-4468-9f67-a9994baab49c" />
<img width="1264" height="560" alt="eg2" src="https://github.com/user-attachments/assets/274e55c1-231e-4bea-9bf6-860fc0d8df42" />
<img width="1242" height="545" alt="eg3" src="https://github.com/user-attachments/assets/534c56eb-d9d7-4204-92c5-5ada7e483fd0" />

## Inspiriation
Our idea for "Odyssey" was a mix of a musical odyssey and a travel odyssey. We wanted to take the user on a journey through music, while they themselves were on a journey through space.
What it does

## What it does
The user selects two points on a map where a journey line is drawn between them. Once they submit their desired start and end points the program will randomly pick cities along the journey within a radius of the journey line. Then through the program finds a number of top songs from each city and recommends them to the user with Spotify links. It also displays some details of the journey, these are the number of unique artists, the number of cities visited and the total number of tracks.
How we built it

## How we built it
The program was written in Java using Spring Boot in order to create a web app. We used Open Street Maps and Leaflet to display a map to a screen and get the longitude and latitude of a selected route. We used Nominatim to get nearby cities along the route, then filtered and sorted by "importance" (An OpenStreetMaps metric). Using LastFM we got some of the top songs in the area and used the Spotify API to get further data. We then displayed all this information on the Leaflet OpenStreetMaps map.
Challenges we ran into

## Challenges we ran into
We found that most cities have the same top charts, making the playlists a bit boring. To avoid this, we got a random amount of songs from the top 30, and removing duplicate entries. We found it challenging to work with the LastFM API as the country names required to get city data was both not clear, and also not the same as in Nominatim. This lead to us having to implement a map and doing trial and error in order to complete it. We were limited by the number of requests per second we could do to crucial APIs, such as the Nominatim API. This meant we had to create a loading screen to occupy the user while we slowly sent our requests.
Accomplishments that we're proud of

## Accomplishments that we are proud of
We are proud that the system pulls good results along the chosen route. We are happy that we ended up getting multiple APIs to work in tandem, with only a few unintended results.
What we learned

## What we learned
There is a large difference in the documentation of APIs, and many APIs need a lot of care in order to be used properly
