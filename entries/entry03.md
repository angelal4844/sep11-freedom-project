# Entry 3 (Tinkering with kaboomjs (Day3))
##### 2/13/2023

## Context 
These few weeks, I was tinkering with kaboomjs and working on my project that I made using kaboomjs. Last blog, I was loading all the sprite, calling the sprite, and creating a easy level using `addLevel([])` for my game. This blog, I will talk about how I made the sprite interactive.


## Kaboomjs (Day 3) 
* `onKeyPress()` --> 
* `onKeyDown()`--> helps the sprite move up, left, down, or right
* `onMouseDown()` --> helps move the sprite to the place you clicked
* `onClick()` --> when you click on the sprite, it can help make a sound or open something
* `const x = rand(0, width())` --> Helps move the sprite in different places horizontally. 
* `const y = rand(0, height())` --> Helps move the sprite in different places vertically.

## Game 
In the beginning, when I was trying to make my sprite interactive, I was really confused what was the difference between `onKeyDown()` and `onKeyPress()`. In addition, I tried it in kaboomjs playground and learned that onkeyDown() helps the sprite go to different directions, while onKeyPress() helps the sprite move anywhere when you click on any keys. 

First, I started making the sprite move in random places. I used 
```JS
const x = rand(0, width())
const y = rand(0, height()) 
```
When I run the game, the mushrooms were moving in different places.

(First time)

(Second Time)

Then, I tried using `onKeyDown()`
``` JS
onKeyDown("left", () => {
    tree.move(-SPEED, 0)
})
```
When I run it, it said that tree was not defined 

In addition, I learned that you need to add a sprite before calling the sprite. 
``` JS
const player = add([
	sprite("tree")
])
onKeyDown("left", () => {
    tree.move(-SPEED, 0)
})
``` 
Then, I tried using `onMouseDown()`.
`onMouseDown()` is similar to `onKeyDown()`. In `onKeyDown()`, you can use but when you use your mouse to click somewhere, the sprite will follow the direction you just clicked. 
``` JS
onMouseDown("down", () => {
	player.move(3, SPEED)
})
```
Lastly, I tried using `onClick()`, where when you click on the object, it creates a sound or makes the object interactive.
``` JS
onClick(("door") => go("game"))
```
When you click on door, it goes back to the first level.
## Skills 

## EDP



[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
