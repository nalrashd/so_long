# so_long

<img width="148" alt="Screen Shot 2022-10-27 at 4 48 53 PM" src="https://user-images.githubusercontent.com/101207512/198288676-75544726-b480-451f-9033-43d1ad8a898f.png">

This projects goal is to create your own 2D game where you have a map that can have different dimensions and contents.<br>

### Requirements to run the game
Only tested on **macOS Catalina (Version 10.15.7)**.<br>
For all other OS it is not guaranteed to work.<br>
OpenGL and AppKit is required to run it.<br>
If you want to run it on Linux [here](https://harm-smits.github.io/42docs/libs/minilibx/getting_started.html#compilation-on-linux) is a tutorial that might help and [here](https://github.com/42Paris/minilibx-linux) is the required version of miniLibX, this is **not tested** with my so_long.<br>

### Map
A valid map is structured as followed:<br>
- 1 player (`P`)
- at least 1 exit (`E`)
- at least 1 collectible (`C`)`
- is recatangular
- has a solid outside border out of walls (`1`)
- all the empty spaces are filled with `0`
- map has to be `.ber`
- no other characters than:
  * `P`
  * `E`
  * `C`
  * `1`
  * `0`
- i.e. `map.ber`:
- one new line after the map is valid, if there is anything else, it is not valid

```
1111111111111111
10C1110000000001
10111000C00C0001
1011000000000C11
1C10000011101111
100001CCC1P00E11
1111111111111111
```

<br>

### During the game
The player can only be moved by `WASD`.<br>
The player can not move into walls.<br>
The player can only exit if all collectibles are collected.<br>
The amount of movements is counted and displayed in the terminal.<br>
Every try to move even if it is invalid will be counted as one move.<br>

All the visualization is done with the help of the [MiniLibX library](https://github.com/tblaase/so_long/tree/master/mlx "https://github.com/tblaase/so_long/tree/master/mlx").

<br>

To run this project please follow the following steps:
- make
- ./so_long maps/map.ber

This is how the game looks

<img width="1203" alt="Screenshot 2023-02-21 at 9 48 13 AM" src="https://user-images.githubusercontent.com/101207512/220309178-64ae873b-7c1f-4e98-bdee-69e3f3f512c6.png">

This is what will be written in the terminal during the game when you successfully win the game.

<img width="364" alt="Screenshot 2023-02-21 at 1 55 08 PM" src="https://user-images.githubusercontent.com/101207512/220311591-696c5ca0-98e7-4407-8a1e-fafc6c0e3b81.png">

I hope that this project will benefit you by gaining sufficient information.
