# music-player
Create beautiful UI to play music stored in the "music folder" using the HTML5 audio API

## Description

This is a JavaScript code that creates a music player with controls for playing, pausing, skipping to the previous or next song, and displaying the current progress of the song being played.

The code starts by defining variables for the different elements of the music player, such as the music container, play button, previous button, next button, audio element, progress bar, progress bar container, title, and cover.

Next, it defines an array of song titles and initializes a variable called songIndex to 2, which is used to keep track of the current song being played. The `loadSong` function is then called to load the song details of the initial song into the DOM.

The `playSong` and `pauseSong` functions are used to play or pause the audio, respectively. When the play button is clicked, the `playSong` function is called, which adds a class of play to the music container, changes the play button icon to a pause button icon, and starts playing the audio. When the pause button is clicked, the `pauseSong` function is called, which removes the play class from the music container, changes the pause button icon to a play button icon, and pauses the audio.

The `prevSong` and `nextSong` functions are used to skip to the previous or next song, respectively. When the previous button is clicked, the `prevSong` function is called, which decrements the `songIndex` variable, checks if it goes below `0`, and if so, sets it to the last song in the array. It then loads the song details of the new song and starts playing it. Similarly, when the next button is clicked, the `nextSong` function is called, which increments the songIndex variable, checks if it goes above the length of the array minus 1, and if so, sets it to the first song in the array. It then loads the song details of the new song and starts playing it.

The `updateProgress` function is used to update the progress bar as the song plays. It gets the duration and current time of the audio element and calculates the progress percentage, which is used to update the width of the progress bar.

The `setProgress` function is used to allow the user to click on the progress bar and skip to a particular time in the song. It gets the width of the progress bar container, the position of the click, and the duration of the audio element, and sets the current time of the audio element accordingly.

Finally, event listeners are added to the play, previous, and next buttons, as well as the audio element and progress bar container. When the play button is clicked, it toggles between playing and pausing the audio. When the previous or next button is clicked, it skips to the previous or next song, respectively. When the audio element's time updates, it updates the progress bar. When the progress bar container is clicked, it skips to a particular time in the song. And when the current song ends, it automatically skips to the next song.
