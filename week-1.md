# Week 1 (1st week of June)

## Getting Started

### Project Overview

My project involves developing eight math activities for the Sugar desktop environment. 
> Sugar is a desktop environment, and activities in Sugar are the equivalent of apps on Android or programs on Windows.

The activities are inspired by Alexander Bogomolny's work as archived [here](https://www.cut-the-knot.org/). It will help children learn different difficult math concepts like, Pascal triangle, graph theory, latin squares and many other complex mathematical notions in a gamified and visually child friendly manner.

Here is the list of activities to be developed during the GSoC 2024 period:

1. **[Nim Game](http://www.cut-the-knot.org/nim_st.shtml)**
2. **[Lewis Carroll's Game of Logic](http://www.cut-the-knot.org/LewisCarroll/LCGame.shtml)**
3. **[The Candy Game](http://www.cut-the-knot.org/Curriculum/Algebra/IntergerIterationsOnACircle.shtml)**
4. **[Number Guessing Game](http://www.cut-the-knot.org/Curriculum/Algebra/Cards.shtml)**
5. **[Latin Squares](http://www.cut-the-knot.org/Curriculum/Algebra/Latin.shtml)**
6. **[Pascal Triangle Visualization](http://www.cut-the-knot.org/Curriculum/Algebra/DotPatterns.shtml)**
7. **[Three Utilities Puzzle](http://www.cut-the-knot.org/do_you_know/3Utilities.shtml)**
8. **[Illusion Box](https://www.cut-the-knot.org/Curriculum/index.shtml#illusions)**


## River Crossing Activity

Github Repo: [https://github.com/marsian83/river-crossing-activity](https://github.com/marsian83/river-crossing-activity)

Inspired by the [Goat, Cabbage, and Wolf](http://www.cut-the-knot.org/ctk/GoatCabbageWolf.shtml) puzzle, I have developed a river crossing activity for Sugar. The game involves a farmer trying to cross a river with his belongings. This activity is implemented in a modular manner, allowing for easy addition of more levels, characters, and themes.

#### Implementation Details

- **Logic**: 
  - Implemented an update system logic to separate `views` and `components`. 
  - **Views** describe the currently opened page/screen.
  - **Components** describe the various parts within a view.
  
- **Generic Classes**: 
  - `Drawable`: Facilitates creation of objects to be drawn on the display surface.
  - `Clickable`: Encapsulates logic required to create on_click events for objects.
  - `ContainerBox`: Acts as an automatic flowing container that justifies and positions items automatically and symmetrically.

These classes will be used for future activities, including those specified in this proposal. The framework developed through this project will not only support the current activities but will also be adaptable for future projects. Stay tuned for updates on additional features and enhancements!

#### Demo

The video below shows a demo of the fully working activity. I plan to add settings, themes, and sound to this activity soon.

[![River Crossing Activity Demo](https://github.com/marsian83/GSOC-24-report/assets/114365550/96341806-d26a-48ff-b8f3-de4380d3590f)](https://github.com/marsian83/GSOC-24-report/assets/114365550/96341806-d26a-48ff-b8f3-de4380d3590f)

> The assets used in the game are self-designed.


## Nim Game

Github Repo: [https://github.com/marsian83/nim-game-activity](https://github.com/marsian83/nim-game-activity)

Inspired by the [Nim](https://www.cut-the-knot.org/nim_st.shtml) game, I have started the development of the Nim game activity for Sugar. The activity will consist of an item which will be arranged in rows and each participant will take turns removing a number of these items. The participants will be the user and the computer (Robot). The last person to remove an item will win the game.

![image](https://github.com/marsian83/GSOC-24-report/assets/114365550/b078ea74-6286-4b07-b899-420cff67df65)
> Possible User interface for the game

### Current Progress
The project's folder structure and code sctructure have been consolidated and I have added an easy mode (AI plays randomly)

The AI for this game will be implemented using the [“Winning Arithmetic Progression” aka “Zero Nim sum” concept](https://www.archimedes-lab.org/How_to_Solve/Win_at_Nim.html#:~:text=Two%20players%20take%20any%20number,of%20the%20rows%20remains%20ZERO.) used by many Nim-like games.

The logic for rendering the board, picking out object rows and importing of generic images to represent nim objects has also been implemented.


