# mazegen

a very simple text/menu-based maze game engine, written in the [willow programming language](https://github.com/weepingwitch/willow/)

## usage
regular usage:
```bash
python willow.py mazegen.py
```

passing in a maze file:
```bash
python willow.py mazegen.py maze_file.maze
```

try passing in "mazes/sample.maze"

## maze files
you can create your own maze files using a simple syntax.

each maze is made up of a series of labels. every maze must at least have a label 0 - that is where the maze begins.

### labels
labels are the basic units of a maze. you can think of them as rooms.

each label must have at least one choice defined.

define a label (and choices) like this:
```
LABEL 0
TEXT You are in a room. There is a red door and a blue door.
CHOICE Red Door
GOTO 5
CHOICE Blue Door
GOTO 6
```
the TEXT is the description that will be printed out when the user reaches that label, while the CHOICEs (and their associated GOTOs) create the options that the user will have to pick between. in this case, if the user types in 1, she will go to label 5, but she types in 2, she will go to label 6.

it is possible for labels to have only one choice:
```
LABEL 7
TEXT You are in a dark, dark cave.
CHOICE Walk forward.
GOTO 9
```
in this case, the user only has one option - meaning that she will have to type in 1, and go to label 9.

have fun making your own mazes!
