# Rush Hour Solver :blue_car: :car: :taxi: :articulated_lorry:

This is a command line utility to solve
[Rush Hour](https://en.wikipedia.org/wiki/Rush_Hour_(puzzle)) puzzles.

## Usage

The starting positions of the automobiles are passed to the script by providing
arguments of the form `name,model,x,y` for each automobile.
The names must be unique.
The model must be one of `hcar`, `hbus`, `vcar`, or `vbus`.
The name `hcar` stands for "horizonal car", etc.
The coordinate `x`,`y` specifies the leftmost/topmost coordinate of the automobile
(the coordinates each start at 1).

## Examples:

The puzzle:

```
aa...b
c..d.b
cRRd.b
c..d..
e...ff
e.ggg.
```

can be solved with:

```
./rushhour --player-car R R,hcar,2,3 a,hcar,1,1 b,vbus,6,1 c,vbus,1,2 d,vbus,4,2 e,vcar,1,5 f,hcar,5,5 g,hbus,3,6
```

And a much harder puzzle:
```
./rushhour red,hcar,4,3 yellow,vbus,1,1 blue,hbus,1,4 lavendar,vbus,6,2 olive,hcar,2,1 light_blue,vcar,2,2 pink,vcar,3,2 orange,vcar,5,1 purple,vcar,4,4 tan,hcar,1,6 green,vcar,3,5 lemon,hcar,4,6 black,hcar,5,5
```

To display a puzzle instead of solving it, use the `--display` flag:
```
./rushhour red,hcar,4,3 yellow,vbus,1,1 blue,hbus,1,4 lavendar,vbus,6,2 olive,hcar,2,1 light_blue,vcar,2,2 pink,vcar,3,2 orange,vcar,5,1 purple,vcar,4,4 tan,hcar,1,6 green,vcar,3,5 lemon,hcar,4,6 black,hcar,5,5 --display
```
