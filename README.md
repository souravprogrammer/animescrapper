# Anime Scrapper
[![Build Status](https://travis-ci.com/souravprogrammer/animescrapper.svg?branch=master)](https://travis-ci.com/souravprogrammer/animescrapper)

Anime Scraper is a library that provides unofficial api to scrape anime streaming platform like <a href="http://www.anime1.com">anime1</a> 

This project is created fo the purpose of using it into <a href=""> Doge San.</a>

# How to use 

    // initalize the object
    Anime anime = Anime.createInstance(); // returns anime object
       
 


  ### All Anime List


    List<AnimeList> list = anime.getAllAnime(); //returns all anime 
       
       
 ### Search Anime List
    List<AnimeList> searchedlist =  anime.getAnime("<name of your anime>"); // returns all AnimeList
    object that match your search. 

 ### Anime Card
 ###### anime card is an object that holdes all the info about anime like episodes , title, description , image url.
    //aniime path 
    String anime_path  = list.get(0).getPath();
    AnimeCard animecard = anime.getAnime(anime_path);
    
 ### Video Stream Url
     List<Episodes> episodes = animeCard.getEpisodes();
     String stream_url = Anime.getEpisodeStream(episodes.get(0).getPath()); 
     
 # Library Used
 * Jsoup
 
 # important classes
 
 Class          | Methods
 ---------------|--------------------
  AnimeList     | getTitle() , getPath()
  AnimeCard     | getTitle() , getDescription() ,getImg_path(),getEpisodes() 
  Episodes      | getPath()  , getEpisodeNumber() 
  AnimeSlide    | getGif_path() // AnimeSlide is a chid class of AnimeList
 
 
 # Contribution
 Want to contribute? Great!

Fork your own copy of this repository, make changes, update, fix bugs, add additional features or just prettify the code and create a pull 
request explaining what have you added fixed or improved so that we can merge it to our branch.
 
 # IMPORTANT NOTE

 This is API in created without the consent of the owner of the websites, the main purpose of this project was for me to learn webscraping,
 so if you want to use our API, we are not be held responsible for any legal action taken on you by the owner.
