# Entry 3 (Tinkering with kaboomjs (Day3))
##### 2/13/2023

## Context 
These few weeks, I was tinkering with kaboomjs and working on my project that I made using kaboomjs. Last blog, I was loading all the sprite, calling the sprite, and creating a easy level using `addLevel([])` for my game. This blog, I will talk about how I made the sprite interactive.


## Kaboomjs (Day 3) 
* `onKeyPress()` --> helps move anywhere when you click on any keys
* `onKeyDown()`--> helps the sprite move up, left, down, or right
* `onMouseDown()` --> helps move the sprite to the place you clicked
* `onClick()` --> when you click on the sprite, it can help make a sound or open something
* `const x = rand(0, width())` --> Helps move the sprite in different places horizontally. 
* `const y = rand(0, height())` --> Helps move the sprite in different places vertically.

## Game 
In the beginning, when I was trying to make my sprite interactive, I was really confused what was the difference between `onKeyDown()` and `onKeyPress()`. In addition, I tried it in kaboomjs playground and learned that `onkeyDown()` helps the sprite go to different directions, while `onKeyPress()` helps the sprite move anywhere when you click on any keys. 

First, I started making the sprite move in random places. I used 
```JS
const x = rand(0, width())
const y = rand(0, height()) 
```
When I run the game, the mushrooms were moving in different places.

(First time) <br>
<img width="732" alt="Screen Shot 2023-02-12 at 2 53 02 PM" src="https://user-images.githubusercontent.com/91750609/218362868-fba16bc0-0592-454b-8bd8-08ce16b43359.png">
</br>
(Second Time) 
<br>
<img width="616" alt="Screen Shot 2023-02-12 at 2 52 43 PM" src="https://user-images.githubusercontent.com/91750609/218362951-dd4cb0f6-4389-4a38-a009-1fdb60bebd8c.png"> 
</br>
Then, I tried using `onKeyDown()`
``` JS
onKeyDown("left", () => {
    tree.move(-SPEED, 0)
})
```
When I run it, it said that tree was not defined 
<br>
<img width="468" alt="Screen Shot 2023-02-12 at 2 50 08 PM" src="https://user-images.githubusercontent.com/91750609/218362979-9d8dae67-fb17-4046-b5d5-bf5efe8efb44.png">
</br>

In addition, I looked at different examples in kaboomjs playground and learned that when using `onKeyDown()`, you need to add the sprite first before calling the sprite. 
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
In this code, when you click on door, it goes back to the first level.
## Skills 
One skill I learn is debugging. When I was making my sprite interactive, my `onKeyDown()` wasn't working because my tree was not defined. In addition, I looked at different examples and try tinkering on my own and found out that you need to add the sprite before using `onKeyDown()`. Another skill I learn is problem decomposition. When I was making the game, I plan out what I want to make every week. Lastly, I also learn time management. These few weeks, I was tinkering and working on 2 events on kaboomjs every week.
## EDP
Last blog, I was in stage 2, research the problem. This blog, I am still on stage 2, research the problem. These few weeks, I was tinkering with kaboomjs and learned different events in kaboomjs like `onKeyPress()`, `onKeyDown()`, and many more. In addition, last blog, I created a easy level for the game. This blog, I used different events to make the sprite interactive. 


[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
