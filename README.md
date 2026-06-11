## Use React, Redux, Immutable to code Tetris [GAMEBOY]

----
Tetris is a classic game that has always been enthusiastically implemented in various languages. There are many versions of it in Javascript, and using React to do Tetris has become my goal.

Open [https://gameboy.my](https://gameboy.my) to play!


## Game on the experience of optimization
* Experience:
	* Press the arrow keys to move vertically and horizontally. The trigger frequency is different, the game can define the trigger frequency, instead of the original event frequency;
	* Left and right to move the delay can drop the speed, but when moving in the wall smaller delay; in the speed of 6 through the delay will ensure a complete horizontal movement in a row;
	* The `touchstart` and `mousedown` events are also registered for the button for responsive games. When `touchstart` occurs, `mousedown` is not triggered, and when `mousedown` occurs, the `mouseup` simulator `mouseup` will also be listened to as `mouseup`, since the mouse-removed event element can not fire.
	* The `visibilitychange` event, when the page is hidden\switch, the game will not proceed, switch back and it will continue, the `focus` state has also been written into the Redux. So when playing with the phone and the phone has a `call`, the progress of the game will be saved; PC open the game do not hear any other gameover, which is a bit like `ios` application switch;
	* In the game `any` time you refresh the page, (such as the closing the tab or the end of the game) can restore the current state;
	* The only pictures used in the game are ![image](https://img.alicdn.com/tps/TB1qq7kNXXXXXacXFXXXXXXXXXX-400-186.png), all the rest is CSS;
	* Game compatible with Chrome, Firefox, IE9 +, Edge, etc .;
* Rules：
	* You can specify the initial board (ten levels) and speed (six levels) before the start of the game;
	* 100 points for 1 line, 300 points for 2 lines, 700 points for 3 lines, 1500 points for 4 lines;
	* The drop speed of the box increases with the number of rows eliminated (one level for every 20 lines);

 ## Summary
* As a React hand application, in the realization of the process found a small "box" or a lot of details can be optimized and polished, this time is a test of a front-end engineers and the skill of the time carefully.
* Optimization of the direction of both React itself, such as what state is stored by the Redux, which states to the state of the component like; and out of the framework of the product can have a lot of features to play, in order to meet your needs, these will be natural propulsion technology development of.
* An application from scratch, the function slowly accumulate bit by bit, it will build into a high-rise, do not fear it difficult to have the idea to knock on it. ^_^


## Development
### Install
```
npm install
```
### Run
```
npm start
```
The browser will go to [http://127.0.0.1:8080/](http://127.0.0.1:8080/)

### Build
```
npm run build
```

Will build the application in the build folder.
