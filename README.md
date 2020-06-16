# CoronaVirus-Run-the-Game

This is a fun interactive game made by Luke Myers June 2020. 

## Game Rules

Use Space bar to control player. Fly or Run player through the obstacle bars. For each set of bars successfully passed the score increases. After each bar passes the screen the speed of the bars will increment up and slowly start increasing speed to make the game increasingly difficult. This progressive speed game will be paired with progressive rock music in the background. 


### MVP: 

- Small box or emoji that travels though game board and must avoid touching bad virus boxes. If player touches bad boxes game is over. Make re-set button or play button to start a new game. 

    ## Checklist for Pseudo code items 

    1. Use HTML:5 to make the game area.
      - Use 1 div set to make the container for the game board.
      - 1 div set for the player 
      - 1 div set fo each virus obstacle pole ( pole 1 and pole 2)
    2. Outside the game container will the div's for the score, speed, and music controls. 
        - Play / reset button will also be here too. 

    3. For the CSS we will have the following 
        - body , container , player , pole , pole_1 , Pole_2, score_div, restart_btn, & hover.
        - #pole defines the obstacle position, Image,  -50px leaves bars off screen until game starts. 
        - #pole_1 and pole_2 are set to top /bottom 0; to give the obstacle an open gap in the center. 

    4. Game Logic will be Jqery and JavaScript 

    2. Create game variables A) Player  B) Obstacles C) Score D) speed E) Reset Btn F) Music

        - Because this is in JQery I have defined ALL my Variables to the corresponding HTML DOM elements.
        - speed variable is set to 10 
        - Container Height and Width are defined as is the size of the player's box 

    4. Function start game - this defines player - score set 0 - set Game Area to blank and ready.

        - 1St Function to be defined is setting the Game Interval rules
        - When the Poles go out of the container we have to bring them back
        - check if the poles are out of the container with a condition of ( IF pole > Container Width )
        -  Next, pole position must be set to = pole initial position so a new pole will appear after leaving the screen.
        -  Next we have pole.css move ! 

    6. function which defines movement of obstacles. 

        -  Write / add a condition which will change pole height with every new pole
        - var new height = random math method x then take initial pole height + new hight
        - This pole_1 + height and Pole_2 - height to keep the Gap of the two poles even. 
        - Finally we set speed to increase via speed = speed +1. I have Speed text updated to keep track of speed.

    7. Function which defines  movement of player.
        - 1st define go down function so have css for player top to increase by + 5 this pulls player down. 
        - Next we set the key-code for the SPACEBAR which is 32. 
        - Next set function to make every-time spacebar / key-code 32 is pressed the UP function will run. 
        - Up function must  DECREASE css height -10  to pull player up 
        - If player is falling set interval. If spacebar is pressed clear interval go up to let gravity start again. 
        

    8. Collision  handles with & Game Over Conditions 
        - Use collision function ($div1, $div2)
        - It will return true if collision will Pole Div's, else false if NO collision. 
        - Write collision player with pole_1 || or player collision Pole_2 = stop game.
        - Function for stop the game will clear interval of the game + display restart button.
        - Game over will also trigger if CSS Game Board's, " bottom or top " is touched.
        

    9. Update Score
        - Update the SCORE when the Poles have passed the player successfully. 
        - If Pole current position > container width - player_left update Score.text +1.
        - Score update is set to false then set to true  after poles pass player.

    10. Reset Button
        - Restart btn on click + function to relocation reload of player and game. 
        - Reset button was already make withe JQery and appears when Game Over is set to True. 


### Stretch goals:

- Make player a happy face emoji. 
- Make virus a digital picture of the coronavirus. 
- Play music - Down with the Sickness by metal band Disturbed. 
- Track Score 
- Increase game speed and keep track of speed
- Create full intro page with game backstory. Also have a start button with link and graphics. 

11. Intro page made with HTML, CSS Animations. JavaScript used for button timer and background stars. 


### 
- Technologies: HTML, CSS, JavaScript, JQery.

### 
Wire Frame 

![Inital WireFrame ](https://i.imgur.com/14PxZoa.jpg )

### References

- https://www.w3schools.com/graphics/game_images.asp
- https://sharethisurls.com/api/get_song.php?id=tuWBZB:zKE2rB
- https://www.freecodecamp.org/forum/t/how-to-play-mp3-in-the-background-music-automatically/308554/3
- https://css-tricks.com/snippets/css/a-guide-to-flexbox/
- https://css-tricks.com/snippets/css/star-wars-crawl-text/  (StarWars Text)
- https://jquery.com/
- https://www.w3schools.com/jquery/




