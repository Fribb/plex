# Plex Media Server FAQ

This document is to answer the common questions users have in regards to the Plex Media Server application

# Table of Contents
- [Plex Media Server FAQ](#plex-media-server-faq)
- [Table of Contents](#table-of-contents)
  - [Missing Library Items or Missing Metadata](#missing-library-items-or-missing-metadata)
    - [Organizing your Video files](#organizing-your-video-files)
    - [Organizing your Local Assets](#organizing-your-local-assets)
    - [Organizing Trailers and extras](#organizing-trailers-and-extras)
    - [Manual Match or Fix Match](#manual-match-or-fix-match)
    - [Duplicates, Split and Merge content](#duplicates-split-and-merge-content)

## Missing Library Items or Missing Metadata

When you add files to your Plex Media Server then there are a few parts that are working in the background to get your files into the library and to request metadata (like the posters and description) and add that to the correct library item.

1. The Scanner: The Scanner is responsible to scan the folder(s) you have added to your Library and to add any relevant files to your Library as an empty library item
2. The (Metadata) Agent: The Agent is responsible for searching for the name and updating the Library item with the relevant Metadata like the Poster, background image, banners but also Ratings, Description, Tasks etc.

### Organizing your Video files

Plex expects your video files to follow a specific naming convention so that the individual of the file can be identified and added to your Plex library correctly. Those naming conventions are different between each library types as listed below:

* Movies: https://support.plex.tv/articles/naming-and-organizing-your-movie-media-files/
* TV-Shows: https://support.plex.tv/articles/naming-and-organizing-your-tv-show-files/
* Music: https://support.plex.tv/articles/200265296-adding-music-media-from-folders/

Any deviation from this convention could result in Files not being detected or Metadata not being pulled or Metadata Mismatches.

### Organizing your Local Assets

What is expected of your video files also applies to locally stored assets like images used as Poster, Banner or as Background image.

* Local assets for Movies: https://support.plex.tv/articles/200220677-local-media-assets-movies/
* Local assets for TV-Shows: https://support.plex.tv/articles/200220717-local-media-assets-tv-shows/

Locally stored assets would need to be activated in the Metadata Agent Settings (Edit Library -> Advanced -> Use local assets)

### Organizing Trailers and extras

Plex also supports that you can store your Trailers and Extras locally and that they are accessible in the Plex UI as well. How you add Extras and Trailers is explained in the links below:

* Movies: https://support.plex.tv/articles/local-files-for-trailers-and-extras/
* TV-Shows: https://support.plex.tv/articles/local-files-for-tv-show-trailers-and-extras/
* Local Artists and Music Videos: https://support.plex.tv/articles/205568377-adding-local-artist-and-music-videos/

### Adding Subtitles

Plex can also read your local subtitle files that are then added, if correctly named, to the library item.
Note that if the language code is missing, plex will mark this as "unkown" and the automatic language selection in your Account/Server language settings will not be able to select it.

* https://support.plex.tv/articles/200471133-adding-local-subtitles-to-your-media/

### Manual Match or Fix Match

If you notice that Plex didn't add the Metadata or actually added the wrong metadata then you have the ability to correc this through the "Fix Match" or "Manual Match" functionality

https://support.plex.tv/articles/201018497-fix-match-match/

While this is a quick and easy way for you to correct something, it is a sign that you either haven't follow the naming convention as described in the links above, or the naming convention wasn't precise enough to make a/the correct match.

Plex supports "ID matching" in which you can add a Metadata provider identifier to the filename that should be used to specifically match to that Metadata. The following IDs are available:

* tvdb
* tmdb
* imdb

How this can be used is described in the links in the 'Organizing your Video files' Section above.

### Duplicates, Split and Merge content

While the scanner will add a new library item for the newly added files to your library, the Metadata Agent could match it incorrectly to something else. A common reason for this is the already mentioned naming convention. If you, for example, don't add the Year the movie was released in then a movie that was released with the same name in different years, plex would not be able to detect and know which year it should match it with.

If you now have that Movie already in your library then plex would remove that library item and add the video file to your already existing library item by creating a duplicate.

This is one of the reasons why your file/folder count on your harddrive could be different to the number displayed in the Plex Library.

Through filters, you can search for duplicate and merged content as described in the link below

https://support.plex.tv/articles/202393718-how-do-i-find-duplicate-or-merged-content/

If you have duplicates then you can split them apart as described in the link below. If you also have content that should be combined in one library item then you can also merge them manually (also explained in the link below).

https://support.plex.tv/articles/201018248-merge-or-split-items/
