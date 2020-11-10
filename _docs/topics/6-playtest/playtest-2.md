---
title: Methods
permalink: /docs/playtest-2/
---

Several different methods of playtesting
* Informal Individual Testing - You casually show the game to a friend
* Formal Group Testing - You have several people play the game at once and give feedback
* Formal Individual Testing - A focused analysis of single person's first play through the game
* Online Playtesting - Automated analysis of thousands of online play sessions

## Informal Individual Testing

Casually ask a friend if she'd mind trying out your game. 
* Most useful in the early stages of game development
* Great for testing a new feature

### Things to keep in mind during the test
* Don't tell the playtester too much
  * Try just giving her the game and seeing what she does
  * This tests how intuitive your game mechanics are
  * Eventually you'll learn the minimum instruction you need to give
* Don't lead the player
  * Don't ask leading questions that may bias the playtester
  * "Did you notice the health items?" is a leading question
    * Informs the player that there are health items
    * Implies that it's important for her to collect them
* Don't argue or make excuses
  * As with everything in design, your ego has no place in a playtest
  * Listen to all feedback from your testers, especially if you disagree with it
  * This isn't the time to defend your game
  * It is the time to learn what you can from the person who is taking time out of her day to help improve the design improve
* Take notes
  * Keep a small notebook with you & take notes on any feedback you get
  * Especially if it's not what you expected or wanted to hear
  * Collate these notes & look for statements that you heard multiple times
  * If only one playtester said something, don't worry about it as much

## Formal Group Testing

This was once the primary form of testing for large studios. Several people are invited to a lab to play the game. Each person is given an individual station where she can play. Playtesters are given little instruction and start playing. After about 30 minutes, playtesters are stopped and they are then asked to fill out a post-game survey. Investigators sometimes interview the playtesters as well.  

Good for getting feedback from many different people and can also help get many answers to some important questions.

Example post-game survey questions
* "What were your three favorite and three least favorite parts of the game?"
* Provide the playtester with a series of images from the game 
  * "How would you describe the way you felt at these points in the game?"
  * Images are much better for this than trying to describe the location
* "How do you feel about the main character (or other characters) in the game?"
* "Did your feelings about the main character change over the course of the game?"
* "How much would you pay for this game? / How much would you charge for this game?"
* "What were the three most confusing things about the game?"

All formal testing requires a script. The script should answer the following questions:
* What should investigators say to the playtesters to set up the game?
  * What instructions should they give?
* How should investigators react during the playtest?
  * Should they ask questions if they see a playtester do something interesting or unusual?
  * Should they provide any hints to playtesters during the test?
* What should the environment be like for the playtest?
  * How long should the playtester be allowed to play?
* What specific survey questions should be asked of the playtester once the playtest is complete?

Formal investigators should not be part of the development team. All members of the team are already biased about the game. They know how to play, they already know any secret locations or plot twists, they have an emotional investment in people liking the game. Team members could unintentionally bias or lead playtesters.  

Once you've found a good external investigator, keep working with her. This allows the investigator to have insight into the progress of the game and the evolution of playtesters' reactions to the game.  

## Formal Individual Testing

A detailed analysis of a single playtester's experience playing the game. This approach is based on the practices of Usability Testing.  
You record several different simultaneous data streams:
* The game screen - You want to see what the player is seeing
* The playtester's actions - You want to see the control input attempted by the player
* The playtester's face - You want to see the player's emotions
* Audio of what the playtester says - What she says can give you some information about her internal thought process
* Internal game data log - Your game should also be logging time stamped data about its internal state(Covered later in the "Automatic Data Logging" section).

### Running a formal individual playtest

Make test environment similar to the eventual play environment. If testing a console game, give the playtester a couch and large TV. For PC games, a desk and office chair are more appropriate.  

Make the playtester as comfortable as possible. Provide drinks and snacks, restrooms, etc. Tell the playtester how much you appreciate her taking the time to play your game and give you feedback. Ask her to please think out loud. Ask her to help you find the problems with the game.  

After the play session an investigator should sit with the playtester and discuss her experience. Record this session as well.  

## Online Testing

The game must be in the beta phase before beginning large online playtests (often called "Beta Tests"). Remember: Beta means that all known bugs are fixed!

Three forms:
* Closed
  * Invite-only test with a small number of people
  * Find hidden bugs before a larger audience sees the game
* Limited
  * Generally open to anyone who signs up
  * But there are a limited number of spots available
  * Keeps the server from getting overwhelmed
* Open
  * Anyone can sign up
  * The final test of any server before launch

## Playtesting Example

* Skyrates [http://skyrates.net](http://skyrates.net) was developed at Carnegie Mellon by a team of four students. 2008 Gleemax Silver Award for Strategic Gaming at the IGF
* Release Schedule: New release every Wednesday
  * Even Weeks - Started new round; added features
  * Odd Weeks - Bug fix releases (fixed the new features)
* 16-Week Initial Development Time (for v1 of the game):
  * Week   8 - Closed online test (12 playtesters in the same building)
  * Week 10 - Closed online test (25 playtesters in the same building)
  * Week 12 - Closed online test (50 playtesters in various locations)
  * Week 14 - Limited online test (125 playtesters)
  * Week 16 - Limited online test (250 playtesters)
  * Post-Development - Open online beta test (≈1000 playtesters)

## Other Types Of Testing

### Focus Testing
Gather a group of people in a game's core demographic (a focus group) and get their reaction to a prospective game's:
* Look
* Premise
* Music
* Or other aesthetic or narrative elements
Sometimes used by large companies to help determine the business case for development of a game.

### Interest Polling
Use social network sites or crowdfunding sites to poll the level of consumer interest in a game. Can be useful for small companies trying to make sure there is a market for their game. Can also raise funds to complete the game.

### Usability Testing

Tests how well testers can understand and use the interface for a piece of software. Important to also do individual usability testing to investigate how easily the playtester can interact with and gain critical information from your game. This includes testing:
* Various layouts for on-screen information
* Several different control configurations
* Any other aspects of user interface and interaction

### Quality Assurance (QA) Testing
Focused on finding bugs and ways to reliably reproduce them. There is an entire industry devoted to this kind of testing.  
Core elements are:
* Find a bug (a place where the game breaks or doesn't react properly)
* Discover & write down the steps required to reliably reproduce the bug
* Prioritize the bug
  * Does it crash the game?
  * How likely is it to occur for a normal player?
  * How noticeable is it?
* Tell the engineering team so that they can fix it
QA is most often done by the development team and a group of game testers hired for the final phase of a project. It is also possible to set up ways for players to submit bugs but most players don't have the training to generate really good bug reports that include clear steps for reproducing the bug.
