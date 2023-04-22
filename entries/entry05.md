# Entry 5
##### 4/24/23

### Context 
These few weeks, we were continuing on builidng our MVP for our adventure game. We started to create the levels, sprite, character and making the sprite and character move around. In addition, we also made different scenes to make the sprite go to a different level. 

### MVP
After, we finish loading all the sprite, we started builidng the first level for our game. 
``` JS
addLevel([
              
                "                      ",
                "                      ",
                "xxxxxxx          %    ",
                "x      x    xxxxxxxxxx",
                "x       x!           x",
                "x *      x    A      x",
                "x ^ =     x          x",
                "xxxxx      x   ^     x",
                "x      @    xxxxxx   x",
                "x              =     x",
                "x      ^ =           x",
                "xxxxxxxxxxxxxxxxxxxxxx",
            ], {
            width: 60,
            height: 30,
                "x": () => [
                    sprite("bush"),
                    scale(0.79),
                    solid(), 
                    area(),
                ],
                width: 65,
                height: 65,
                "^": () => [
                    sprite("table"),
                    scale(6),
                    solid(),
                    area(),
                ], 
 });
 ``` 
 In the first level, we decided to make a easy level, where the sprite collects all the food on the table wothout touching the evil mouse. After we finish creating the level for level 1, we were making the sprite move around. 
 * We use 
 ```JS

onKeyDown("left", () => {
	player.move(-SPEED, 0)
})

onKeyDown("right", () => {
	player.move(SPEED, 0)
})
  
onKeyDown("down", () => {
	player.move(0, SPEED)
})
```
When the player presses the right, left or down arrow, the sprite moves left, right, or down. However, when I was making the sprite jump, it didn't work. It said that `player.jump is not a function`. 
``` JS
(Before)
 onKeyPress("space", () => {
		player.jump();
});
```
After watching a tutorial on how to make the sprite jump, I learned that you need to 


[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)