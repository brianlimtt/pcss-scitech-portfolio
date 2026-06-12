---
layout: default
title: Learning Logs
---

# Learning Logs

<details style="border:1px solid #ddd; border-radius:10px; padding:15px; background-color:#fafafa; margin-bottom:15px;">
  <summary style="font-size:18px; font-weight:bold; cursor:pointer;">
    Variables & Data Tracking 
  </summary>

  <br>

  <strong> Variables & Data Tracking </strong><br>
1. What concept did you implement? State the topic clearly and include a relevant code snippet.<br>
2. Where did you use it, and why did you implement it that way? Explain the purpose of the code and your reasoning behind the approach you chose.<br>
3. What challenges did you encounter, and how did you fix them? Describe any issues you faced and the steps you took to resolve them<br>
<br>
<br>
1. Concepts I implemented for variables included variables that allowed me to store important information about the player’s progress and update it throughout the game.
"int blobLives = 3;
int stageNum = 1;
int difficultySelected;
blobLives = blobLives - 1;
stageNum = stageNum + 1;"
These variables keep track of the player’s remaining lives, current stage, and selected difficulty level.
<br><br>
2. I used variables throughout the game to monitor player progress and control gameplay. For example, the blobLives variable tracks how many lives the player has left after touching spikes, while stageNum tracks which stage the player is currently on. I did this because variables provide a simple and efficient way to store changing information. Instead of creating separate code for every stage or life count, I could update a single variable and use its value throughout the program.
<br><br>
3. One challenge I encountered was making sure the variables reset correctly when the player restarted the game. Early on, values such as lives and stage number would sometimes carry over from the previous playthrough, causing incorrect game behavior.
<br><br>
To fix this, i created a reset system: 
"void stageReset() {
  blobLives = 3;
  blobSpeed = 4;
  blobSight = 1;
  powerUpX = 20* scale;
  powerUpY = 40* scale;
}"
<br><br>
Whenever the player started a new game or changed stages, this function restored important variables to their default values. This ensured that each game began with the correct settings and prevented data from previous attempts from affecting future gameplay.
<br><br>
  <hr>
</details>


<details style="border:1px solid #ddd; border-radius:10px; padding:15px; background-color:#fafafa; margin-bottom:15px;">
  <summary style="font-size:18px; font-weight:bold; cursor:pointer;">
    Selection Structure
  </summary>

  <br>

  <strong> Selection Structure </strong><br>
1. What concept did you implement? State the topic clearly and include a relevant code snippet.<br>
2. Where did you use it, and why did you implement it that way? Explain the purpose of the code and your reasoning behind the approach you chose.<br>
3. What challenges did you encounter, and how did you fix them? Describe any issues you faced and the steps you took to resolve them<br>
<br><br>
1. Selection structures allow the program to folllow instructions based on specific conditions and execute different code depending on the situation.<br>
   "if (blobLives <= 0) {
    gameEnd();
}if (difficultySelected == 1) {
    tutorialOneOn = true;
} else if (difficultySelected == 2) {
    tutorialOneOn = true;
} else if (difficultySelected == 3) {
    tutorialOneOn = true;
}"
These statements allow the game to react differently based on the player’s actions and current game state.
<br><br>
2. I used selection structures throughout my game to control different events. For example, when the player collides with spikes, the game checks whether they still have lives remaining. If not, the game transitions to the losing screen.
"if (blobLives <= 0) {
    gameEnd();
}"
<br><br>
I chose this approach because it makes the program react to player choices and conditions. Instead of running every part of the game at once, I optimized what was running and what was not overall smoothness of the game.
<br><br>
3.One challenge I encountered was making sure the correct game screens appeared at the right time. Multiple screens could accidentally activate at once because several conditions were true at the same time.
<br>
To fix this, I used if, else if, and Boolean variables to ensure that only one screen or game state was active at a time.
"if (tutorialOneOn) {
    tutorialOne();
} else if (tutorialTwoOn) {
    tutorialTwo();
} else if (diffHardOn) {
    diffHard();
}"
<br>
This solution prevented overlapping screens and ensured that the game progressed in the correct order. 
<br>
  <hr>
</details>


<details style="border:1px solid #ddd; border-radius:10px; padding:15px; background-color:#fafafa; margin-bottom:15px;">
  <summary style="font-size:18px; font-weight:bold; cursor:pointer;">
    Repitition Structure
  </summary>

  <br>

  <strong> Repitition Structure </strong><br>
1. What concept did you implement? State the topic clearly and include a relevant code snippet.<br>
2. Where did you use it, and why did you implement it that way? Explain the purpose of the code and your reasoning behind the approach you chose.<br>
3. What challenges did you encounter, and how did you fix them? Describe any issues you faced and the steps you took to resolve them<br>

<br><br>
1. Repetition structures allow a section of code to run multiple times until a condition is met. In my game, I used a do-while loop to repeatedly generate a random stage until it was different from the previously selected stage.
   <br>
   "void diffInfinite() {
  int nextStage = 0;

  do {
    nextStage = int(random(1, 6));
  } while (nextStage == currentStage);

  currentStage = nextStage;
}"
<br><br>
2. I used this repetition structure in the diffInfinite() method, which controls the Infinite Mode of the game. Every time a new stage is selected, the loop continues generating random stage numbers until it finds one that is different from the current stage. <br>
I chose this approach because it guarantees variety in gameplay and it also allows for the player to infinitely play the game until the either lose by having no lives or they want to quit, allowing friends to compete with one another for the highest score. <br>
<br>
3. The challenge I faced was the stages that kept regenerating as the draw function was being called every frame, causing every new frame to be a new stage in the infinite mode. This would make it practically impossible to fully play a stage without it changing the next frame. 

Unfortunately, this was an issue that I was not able to solve as I did not have enough time to complete all desired features.


  <hr>
</details>


<details style="border:1px solid #ddd; border-radius:10px; padding:15px; background-color:#fafafa; margin-bottom:15px;">
  <summary style="font-size:18px; font-weight:bold; cursor:pointer;">
    Arrays & Data Structures
  </summary>

  <br>

  <strong> Arrays & Data Structures </strong><br>
1. What concept did you implement? State the topic clearly and include a relevant code snippet.<br>
2. Where did you use it, and why did you implement it that way? Explain the purpose of the code and your reasoning behind the approach you chose.<br>
3. What challenges did you encounter, and how did you fix them? Describe any issues you faced and the steps you took to resolve them<br>

<br><br>
1. I used a collection of Boolean variables to track which stage, tutorial, or game screen was currently active.<br>
"boolean tutorialOneOn = false;
boolean tutorialTwoOn = false;
boolean stageOneOn = false;
boolean stageTwoOn = false;
boolean stageThreeOn = false;
boolean stageFourOn = false;
boolean stageFiveOn = false;"

<br>

It was after submission where I reazlied that in this scnario, an array might have been a more efficient way of dispalying my code as all values here were false. 
<br><br>

2. I used these Boolean variables throughout the game to control progression between tutorials and stages.<br>
   "if (stageOneOn) stageOne();
else if (stageTwoOn) stageTwo();
else if (stageThreeOn) stageThree();
else if (stageFourOn) stageFour();
else if (stageFiveOn) stageFive();"
<br><br>
It allowed me to clearly separate different parts of the game. Each Boolean variable represents a specific game state, making it easier to determine which stage should run at a given time.
<br><br>

3. One challenge I encountered was ensuring that only one stage was active at a time. Multiple stage variables could accidentally remain set to true, causing incorrect behavior and the wrongly desired stage loading overtop.<br>
"stageTwoOn = true;
stageOneOn = false;"<br>
This ensured that only one stage was active at a time and allowed the game to progress smoothly. <br>

  <hr>
</details>



<details style="border:1px solid #ddd; border-radius:10px; padding:15px; background-color:#fafafa; margin-bottom:15px;">
  <summary style="font-size:18px; font-weight:bold; cursor:pointer;">
    Use of Custom Functions & Error Checking/Restrictions
  </summary>

  <br>

  <strong> Use of Custom Functions & Error Checking/Restrictions </strong><br>
1. What concept did you implement? State the topic clearly and include a relevant code snippet.<br>
2. Where did you use it, and why did you implement it that way? Explain the purpose of the code and your reasoning behind the approach you chose.<br>
3. What challenges did you encounter, and how did you fix them? Describe any issues you faced and the steps you took to resolve them<br>

<br><br>
1. Cuustom functions allowed me to reuse code throughout my game, while error checking ensured that players could not perform actions that would break the game.<br>
"boolean checkCollision(int objectX, int objectY, int obXlength, int obYlength) {
  if (blobX > objectX && blobX+75 < objectX+obXlength &&
      blobY > objectY && blobY < objectY+obYlength) {
    return true;
  }
  return false;
}" <br><br>
This custom function checks whether the player has collided with another object and returns either true or false.<br>
<br>
2. I used the checkCollision() function throughout the game whenever the player interacted with spikes, powerups, or the sewer exit. <br>
"if (checkCollision(powerUpX, powerUpY, 150, 75)) {
    blobSpeed = 10;
}if (checkCollision(sewerTunnelX, sewerTunnelY, 150, 100)) {
    stageNum = stageNum + 1;
}"<br><br>

I chose to create a custom function because collision detection is needed many times throughout the game. Instead of rewriting the same code repeatedly, I could call a single function whenever I needed to check for a collision.<br>
<br>

3. One challenge I encountered was preventing players from performing actions when they should not be allowed to. For example, I needed to stop the player from jumping repeatedly while already in the air. <br>
"if (keyCode == UP && blobJumping == false) {
    blobFalling = false;
    blobJumping = true;
    velocity.y = -7;
}"
<br><br>

I ended up using a boolean variable to check if the player was in the air already and also made sure that the player could also only jump when the player was on the ground. Without this error checking, players could continuously press the jump key and basically fly overtop of all the obstacles on the map. 

  <hr>
</details>
