# Entry 2 (Tinkering with Kaboom.js Day 2)
##### 12/19/2022

The tool I am going to use for my Freedom Project is Kaboom.js. These few weeks, I was tinkering with Kaboom.js in code.cs50.io and replit. I learned about how to load a sprite, `text(" ")`,`addLevel ([])`, `add[]` and many more. These few weeks, my goal was to plan out what my game will look like and start building my game. During the winter break I'm going to finish making my level for hard and hardest and learn about events, where it helps make the game interactive.  

### Kaboom.js 
* `sprite ("sprite name")` -> Helps call a sprite from loadSprite.
* `loadSprite("name you want the sprite to be", "link to the picture")` -> Helps load a sprite 
```JS
(Loading a sprite)
loadSprite("icecream", "img/ice-cream.png")
(Calling a sprite)
const iceCream = add ([
    sprite ("icecream")
]);
```
* `add([])` -> Helps add a sprite,  
* `pos()` -> The position you want 
* `addLevel ([])` -> Helps create 
* `text(" ")` -> 
* `origin("center")` -> Helps start at the topleft
* `rotate()` -> Helps make the sprite rotate
In code.cs50.io, I created a README.md to plan out what I want to include in my game.
``` 
- 3 levels -> Easy, Hard, Hardest (addLevel ([]))
- 3 sprite -> (ice cream, tree, block)
- door = ^
- tree = $
- block ==
```
When I finish planning, I started to add my sprite (ice-cream.png, tree.png, door.png and block.png) inside of my img folder. Then, I used `loadSprite()` to load my sprite.
``` JS
loadSprite ("icecream", "js/classwork/sandbox/img/ice-cream.png");
loadSprite ("tree", "js/classwork/sandbox/img/tree.png");
loadSprite ("block", "js/classwork/sandbox/img/block.png");
loadSprite ("door", "js/classwork/sandbox/img/door.png");
``` 
When I inspect it using http-server, it said that the sprite was not found. I looked back at my code and saw that the pictures were not inside the img folder. After, I put the pictures inside the img folder, I inspect it again but it was still not working. I was wondering that maybe I was in the wrong folder. So, I tried removing `js/classwork/sandbox/` inside of the loadSprite and it worked. 
```JS
loadSprite ("icecream", "img/ice-cream.png");
loadSprite ("tree", "img/tree.png");
loadSprite ("block", "img/block.png");
loadSprite ("door", "img/door.png");
``` 
After I load the sprite, I started calling the sprite and adding the position of where I want my sprite to start. 
``` JS
const iceCream = add ([
    sprite ("icecream"), 
    pos (40, 60), // the sprite starts at the topleft.
    rotate (3)
])
```
```JS 
const treeSprite = add ([
    sprite ("tree"), 
    pos (300, 200), // the sprite starts at the middle.
    rotate (3)
])
```
```JS
const blockSprite = add ([
    sprite ("block"), 
    pos (400, 300), // the sprite starts at the middle.
    
])
```
```JS
const blockSprite = add ([
    sprite ("door"), 
    pos (500, 400), // the sprite starts at the middle.
    
])
```
After I finish calling the sprite, I started creating my map using `addLevel([])`. 
``` JS
addLevel([
    (level = easy)
    "                           ",
    "                           ",
    "          ^ $  ===         ",
    "         ====      ==      ",
    "                      =    ",
    "               $ $    =====",
    "===========================",
]
```
`^`= door, `$` = tree, and `=` = blocks. 
```JS
"=": () => [
        sprite("block"),
        area(),
        solid()
    ],
"$": () => [
        sprite("tree"),
        area(),
        solid()
],
"^": () => [
        sprite("door"),
        area(),
        solid()
    ]
```
When I finish making my level 1 map, I inspect it using http-server and it worked! 


[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)