# Python bot for playing a mine game

Game by **Yusuf Hüseyin Şahin**

A python script that play a mine game using computer vision techniques. 

In the game, main character is trying to reach the end of the map given below.

<img src="https://github.com/demirkirans/MineGame-BLG453E/blob/main/images/map.png?raw=true" width="800" height="400">

By default the character can be controlled using arrow keys and shift key makes him run faster. I used `pyautogui` library to take screenshots of the board, decide on the next action and simulate these actions. 

The problem with these grids is, some of them are mined. However, if our character is close to a mined grid(according to grid borders), a face image having a "shocked" expression appears on the bottom right as given: 

<img src="https://github.com/demirkirans/MineGame-BLG453E/blob/main/images/closetomine.png?raw=true" width="800" height="400">

Following strategies were used:

* Facial landmark detection used to detect the difference between **shocked** face and **normal** face
* I benefit from edge detection to detect whether the character is entered to another grid.