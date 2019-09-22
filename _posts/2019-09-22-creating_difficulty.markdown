---
layout: post
title:      "Creating Difficulty "
date:       2019-09-22 05:16:25 +0000
permalink:  creating_difficulty
---


The one size fits all approach has been the one approach that always fails when you have different users, In the world of gaming this seems to be even especially true. A task that might be difficult for one player can be a breeze for another. When a game is either too difficult or not much of a challenge the game quickly becomes not fun. The game must hit a sweet spoot for the individuals.

When creating the artificial intellegence (AI) for the CLI tic tac toe game, creating difficulty was one of the major questions I wanted to answer.

<h3>Simple AI</h3>

First we needed to have a working AI, a simple command that would keep the game moving until either a player had won or the game was tied. Lets call this our simple AI. Simple Ai would check the array of open squares on a board and plays the computers token ( X or O) in the first empty square it finds startign from top left of the board and working its way right, going to the next row of the board if the other squares in that row are not empty. (Top row, Middle row then finally bottom row).

<h3> Creating the Unbeatable</h3>

Unsure how to crate an AI that was a bit smarter than our simple AI, creating the other extreme of the spectrum seems like a good direction on where to go next. To create an AI that is unbeatable requires three new ways of looking at the game.

<b> 1. Where should I start? </b>
<b> 2. Can I win? </b>
<b> 3. Should I block? </b>

After playing many games of Tic Tac Toe, I concluded that starting in a corner if the board is empty was the most advantageous move. Playing in the middle if the board was not empty is the second best possible move. And selecting a corner if your opponent started at the middle gave you the best chance to draw. Playing in any of the four cross like spaces between the corners was always the worse opener. To ensure that each game felt and looked a bit different the corner opening should be randomized. 

The main objective in any game with the unbeatble AI is to win.The Can I win logic recognizes if it is possible to win in the next move and to play that space on the board. This logic should be placed after the openers. 

If winning is not possible then preventing a loss and forcing a draw is the second highest priority of an unbetable AI. Should I block, checks if the AI can lose an dplays the blocking move. This logic is placed after the Can I win to stop situations where the AI could win but instead choses to block. 

If neither Can I win or Should I block are possible then the Simple AI plays the next empty space. 

<h3> Finding the middle ground</h3>

If you're a player who is not training to become the best in the world at TicTacToe or you want to play against an opponent who tries a bit more then a middle difficulty is required for our AI. We can take away the Can I win function from the unbeatable AI and force our AI to only block. The game would be a bit more difficult than our simple AI but not impossible to win. 

Bonus* We could make another function that determines if there is a trap is possible and prevents one from being made. This would be a nother level of difficulty for a player to face. 

<h3> Looking forward</h3>

If a player was unsure of their skill level an elo system could be added in the form of a counter. ELO is a system used to measure skill, usually associated with chess to create best matchmaking and determine rankings/requirements for tournements (something outside the scope of our AI for TicTacToe). A player could begin playing the AI and after each game a counter would increase by 1 if the player won a game, by zero if there was a tie and decrease  by 1 should the player lose. After hitting a certain threshold the AI would change to the next level of difficulty. From Simple Ai --> Middle AI(should I block) --> Middle Ai (are there traps?) --> Unbeatable AI.


