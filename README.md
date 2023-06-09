# Simple Lyric Finder
## User Story
**AS** someone who enjoys singing my favorite songs \
**I WANT** to find the lyrics to my favorite songs and have the ability to play that song \
**SO THAT** I can properly sing along to my favorite songs

## Description
Lets users search for song lyrics by providing the song and artist. Lyrics are found by searching the song & artist in Genius's database with the use of Genius's API. Turns out that Genius's API does not provide lyrics, but rather the path to the web page for the lyrics of that song. In order to get the lyrics, the lyrics are scraped straight from the web page using jQuery's .get() method with the additonal help of a CORS proxy API to get around the issue of being blocked by CORS policy. Songs that don't exist in the Genius database leads to a message about the song not being found. While searching a song that does exist, a message saying "Searching..." is displayed. When there's some trouble scraping the lyrics off Genius a message "Trying to reach Genius.com..." is displayed. A bad URL leads to a basic error message. The last searched song is stored locally and is pulled up again the next time the user opens up the page.\
\
Styling was created with both vanilla CSS and Tailwind CSS framework.\
\
There were issues with the Spotify API since it involved OAuth and Node JS, subjects which we haven't covered yet, to create player for a user to sing along to a song, but **our work regarding Spotify API can be found in the spotify-api branch.**

## APIs Used
- Genius API
- CodeTabs CORS Proxy API
- Spotify API (incomplete)

## Screenshots
![Screenshot 2023-05-18 201034](https://github.com/cwchilvers/SimpleLyricFinder/assets/59628271/6615a2ee-0216-482e-82c1-0fc651dc5c48)
![Screenshot 2023-05-18 201054](https://github.com/cwchilvers/SimpleLyricFinder/assets/59628271/f913f327-4985-48f6-9c58-a63c870a5c65)

## Roles
- **UI and Tailwind CSS:** Dung Tran
- **Genius API, CodeTabs CORS Proxy API, Lyric Scraper:** Chandler Chilvers
- **Spotify Web API:** Alvaro Vazquez

## Deployed Web App
[Simple Lyric Finder](https://cwchilvers.github.io/SimpleLyricFinder/)
