## Song Recommender using Spotify API

#### WHAT IS SPOTIPY?

It is a Python library to use the Spotify API.
To install it we need to open a new jupyter cell and type the following:

!pip install spotipy

In order to have access to the API, we need to get our credentials.
- Go to “ developer dasboard”:
- Register for the account
- Get an account
- Create a new App and give it any name and a description
- Get your “Client_ID” and “Client Secret ID” and store them into a *.py file in the same work folder.

#### HOW TO SET UP EVERYTHING:

First we need to initialize Spotipy with our credentials:

sp = spotipy.Spotify(auth_manager=SpotifyClientCredentials(client_id= Client_ID,
                                                       client_secret=Client_Secret))

#### SOME USEFUL FUNCTIONS:

To make searches:
sp.search(q = “user_query”, limit=5 ) 

Searches can be done by: topic, href, id, uri
It returns a dictionary which can be seen easier with: codebeautify

If we would like to search for a given playlist, we can use the following function:

sp.user_playlist_tracks("spotify", "playlist_id")

Getting the audio features of a song:
sp.audio_features(song["tracks"]["items"][0]["uri"])[0] (it can accept a list of ids, 100ID max)
Which is another dictionary with the AudioFeaturesObject






