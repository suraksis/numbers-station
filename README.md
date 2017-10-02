# Numbers Station

## Introduction
This challenge is for the SOFWERX escape room - a rather simple [Book Cipher](https://en.wikipedia.org/wiki/Book_cipher) in which a specific book is our key.  As the participants will not be the intended recepient, part of the challenge will be to first identify which book should be used.  The announcer has a Russian accent which should lead to the Soviet-era book nearby in the room.

The `audio` folder contains recordings of separate number sets, the full message.mp3 file, and the audacity project for future editing.

## The Book
As with any book cipher, the book is a critical component and as with any escape room, authenticity is just as important.  For this challenge we are using a soviet-era book written by А.И. Палий (A.I. Pali) _Радиовойна_, (_Radio War_) published in 1963 by the Ministry of Defense of the USSR in Moscow. The book will be provided to participants and is shown below:

![The Radio War](/img/cover.jpg)

## Cipher
As with tradition, groups of three numbers will be transmitted, like (25, 8, 3) - representing the twenty-fifth page, eighth line, third word.  As we use words, rather than just characters, the message will be in the format of "(The|This) (Flag|Key|Password|Code) Is ____", granted this message will be in Russian and will need to be translated.

## Sound File Generation
While we could use a universal text to speech generator like `pyttsx`, I've chosen to use the Mac OS text to speech Accessibility utility as it has a higher quality and allows a Russian accent to lend more to the overall scenario.  Due to the accent and to reduce difficulty, all numbers are singular, instead of seventeen for example, we say one seven. Sound file generation is done with the following process in Mac OS:

  - Set System Settings -> Accessibility -> Speech -> System Voice to Milena with Speaking Rate between the first and second notches.
  - In terminal, `say number number -o numbernumber.aiff` e.g. `say one two -o 12.aiff`.
  - Use `lame` to convert the aiff to mp3s.
  - Combine mp3s with appropriate pausing in your favorite audio editing program, I'm using Audacity.

## Challenge
Due to the time constraints, the challenge is as straight forward as possible:

  1. Get the Numbers
  2. Use the book to obtain the message
  3. Translate message from Russian to English
  4. Obtain the code word from the message

<details>
  <summary>Spoilers - Current Challenge</summary>
  
  ```
  (36, 2, 4) - это
  (27, 1, 3) - КОДОВЫХ
  (74, 5, 3) - передатчиков

  Assembled: это КОДОВЫХ передатчиков

  (this | it is) CODE transmitters
  ```

</details>

