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
1. What concept did you implement? State the topic clearly and include a relevant code snippet.
2. Where did you use it, and why di dyou implement it that way? Explain the purpose of the code and your reasoning behind the approach you chose.
3. What challenges did you encounter, and how did you fix them? Describe any issues you faced and the steps you took to resolve them

1. Concepts I implemented for variables included variables that allowed me to store important information about the player’s progress and update it throughout the game.
"int blobLives = 3;
int stageNum = 1;
int difficultySelected;
blobLives = blobLives - 1;
stageNum = stageNum + 1;"
These variables keep track of the player’s remaining lives, current stage, and selected difficulty level.

2. I used variables throughout the game to monitor player progress and control gameplay. For example, the blobLives variable tracks how many lives the player has left after touching spikes, while stageNum tracks which stage the player is currently on. I did this because variables provide a simple and efficient way to store changing information. Instead of creating separate code for every stage or life count, I could update a single variable and use its value throughout the program.

3. One challenge I encountered was making sure the variables reset correctly when the player restarted the game. Early on, values such as lives and stage number would sometimes carry over from the previous playthrough, causing incorrect game behavior.

To fix this, i created a reset system: 
"void stageReset() {
  blobLives = 3;
  blobSpeed = 4;
  blobSight = 1;
  powerUpX = 20* scale;
  powerUpY = 40* scale;
}"

Whenever the player started a new game or changed stages, this function restored important variables to their default values. This ensured that each game began with the correct settings and prevented data from previous attempts from affecting future gameplay.

  <hr>
</details>


<details style="border:1px solid #ddd; border-radius:10px; padding:15px; background-color:#fafafa; margin-bottom:15px;">
  <summary style="font-size:18px; font-weight:bold; cursor:pointer;">
    Selection Structure
  </summary>

  <br>

  <strong> Selection Structure </strong><br>
1. What concept did you implement? State the topic clearly and include a relevant code snippet.
2. Where did you use it, and why di dyou implement it that way? Explain the purpose of the code and your reasoning behind the approach you chose.
3. What challenges did you encounter, and how did you fix them? Describe any issues you faced and the steps you took to resolve them

1. One concept I implemented was selection structures (if/else statements). Selection structures allow the program to folllow instructions based on specific conditions and execute different code depending on the situation.
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

2. I used selection structures throughout my game to control different events. For example, when the player collides with spikes, the game checks whether they still have lives remaining. If not, the game transitions to the losing screen.
"if (blobLives <= 0) {
    gameEnd();
}"

I chose this approach because it makes the program react to player choices and conditions. Instead of running every part of the game at once, I optimized what was running and what was not overall smoothness of the game.

3.One challenge I encountered was making sure the correct game screens appeared at the right time. Multiple screens could accidentally activate at once because several conditions were true at the same time.

To fix this, I used if, else if, and Boolean variables to ensure that only one screen or game state was active at a time.
"if (tutorialOneOn) {
    tutorialOne();
} else if (tutorialTwoOn) {
    tutorialTwo();
} else if (diffHardOn) {
    diffHard();
}"

This solution prevented overlapping screens and ensured that the game progressed in the correct order. 

  <hr>
</details>


<details style="border:1px solid #ddd; border-radius:10px; padding:15px; background-color:#fafafa; margin-bottom:15px;">
  <summary style="font-size:18px; font-weight:bold; cursor:pointer;">
    Repitition Structure
  </summary>

  <br>

  <strong> Repitition Structure </strong><br>
1. What concept did you implement? State the topic clearly and include a relevant code snippet.
2. Where did you use it, and why di dyou implement it that way? Explain the purpose of the code and your reasoning behind the approach you chose.
3. What challenges did you encounter, and how did you fix them? Describe any issues you faced and the steps you took to resolve them

   



  <hr>
</details>
