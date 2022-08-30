# PölderBash Game (Didactic adventure game written in Bash)

![PölderBash Logo](https://github.com/slashdotted/polderbash/raw/master/images/logo.png)

## Introduction
Welcome to Pölder Bash, an adventure game written in Bash that can be used to assess your knowledge of Bash (and more!). This game is comprised of a server, a CLI client (where you can input your commands), and a GUI (in a web browser)

![PolderBash Screenshot](https://github.com/slashdotted/polderbash/raw/master/images/screenshot.png)

## Requirements
Pölder Bash requires a Linux Distribution and some additional tools, namely *realpath* and *socat*. If you are using Ubuntu Linux you can install them using 
```bash
sudo apt-get install realpath socat
```
You can also enable sound effects by installing the *ubuntu-restricted-extras* package.

## Running the game
The game is launched using the *start* script. You need to provide the path to the file containing the gameboard you want to play:
```bash
./start levels/bash_level1.poe
```
## Playing the game
The user interface is comprised of a terminal window (the same where you launched the *start* script) and a web browser. The user interface can be accessed by visiting the following Url: **http://localhost:8183**.

During the game you will need to move Pöldo (or one of the other characters) through a maze. There are doors that need to be opened in order to reach the exit portal (the blue vortex). In your journey you can also collect stars. Doors are opened by answering a question (you can read the question by clicking on a door). 

## Commands
To move your character one step forward you need to execute **pol_forward**. You can turn clockwise or counterclockwise by means of **pol_clockwise** and **pol_anticlockwise**. You can also change your character using **pol_persona**: this command accepts an additional numeric value (from 0 to 9) which corresponds to a different character. 

To open a door we either need to execute some commands (that will automatically unlock the door), or answer a question. To answer a question turn your character toward the door and then use the **pol_say** command followed by the answer (typically a letter), for example **pol_say A**. If the answer is correct the door will be unlocked and you will be able to proceed using **pol_forward**.

## Copyright and license

(c) 2016-2019 Amos Brocco

License: see files

Contact: Amos Brocco <amos.brocco |at| supsi.ch>
