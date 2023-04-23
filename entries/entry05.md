# Entry 5
##### 4/24/23

### Context 
These few weeks, we were continuing on builidng our MVP for our adventure game. We started to create the levels, sprite, character and making the sprite move around. In addition, we also made different scenes to make the sprite go to a different level. 

### MVP
In the last blog, we were loading all the sprite and creating the background. In this blog, we started builidng the first and second level of our game. First, we created a scene for level 1 and 2 using ` scene(" ", () => {}`.In the first level, we decided to make a easy level, where the sprite collects all the food on the table without touching the evil mouse. 
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
In addition, in the second level, we decided to create a harder level by adding spike inside the level. 
``` JS
addLevel([
		            "  -                   ",
                "  ^ =                 ",
                "xxxxxxx          %    ",
                "x      x    xxxxxxxxxx",
                "x       x      A     x",
                "xxxx     x           x",
                "x             = ^    x",
                "x  )    x  xxxxxxxxx x",
                "x ^     xxxx  &      x",
                "xxxx   xxxxxxxxxxxxx x",
                "x    #               x",
                "xxxxxxxxxxxxxxxxxxxxxx",
            ], {
            width: 60,
            height: 40,
        // setting up the label for the sprite, each label corresponds to a symbol in the keyboard, so later on, when we are building the scene (layout), we can just use the coressponding symbol.
                "x": () => [
                    sprite("block-8"),
                    scale(3.7),
                    solid(), 
                    area(),
                ],
```
 After we finish creating the level for level 1 and 2, we started making the sprite move around. 
 * We use `onKeyDown("",() => {})` to make the sprite move when the player presses the key. 
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
After watching a tutorial on how to make the sprite jump, I learned that you need to create a `JUMP_FORCE` on how high you want the sprite to jump when the player presses space. 
``` JS
(After)
const JUMP_FORCE = 500
onKeyPress("space", () => {
		player.jump(JUMP_FORCE);
});
```
After we finish making the sprite move, we started to make the food disappear when we touch the sprite. We used `player.collides() => {}`, where when the sprite touches the bread, the bread disappear. 
``` JS
player.collides('bread', (b) => {
        destroy(b)
}
``` 
After we finish making the sprite collide, we started connecting all the scenes together. We used player.collide( go("scene name")), so when the sprite collides with the object, it goes to the scene. In our adventure game, we created 3 different scenes.
* scene 1(Level 1) --> ("win")
    * when the sprite collides with the door in the first level, it goes to the second level.
``` JS

```
* scene 2 (Level 2) --> ("win-2")
    * When the sprite collides with the door in the second level, it goes to the scene that said "win-2"
```JS
```

* scene 3 (Spike) --> ("lose")
    * When the sprite jump into the spike, it will go to the scene called "lose". 
``` JS
scene("lose", () => {
  // background 
     add ([
     sprite("background3", {width: width(), height: height()}) // 
  ])
  // when the sprite jump into a spike, it will say "You jumped into a spike"
  add ([
    text("You jumped into a spike")
  ])

  keyPress("backspace", () => {
    go("win")
  })
  ```
  Lastly, after we finish connecting all the scenes, we started to create the scoreboard for the sprite. First, we created a variable called score, where score = 0 (initial number). 
  ``` JS
  let score = 0
      const scoreLabel = add ([
        text(score), 
        pos(1050, 0)
      ])
``` 
In addition, everytime the sprite collides with the food, it add 1 to the score. However, when I tried creating the score, it didn't add 1 everytime the sprite collides with the food. 
``` JS
player.collides('egg', (e) => {
  destroy(e)
  score++
  scoreLabel.text = score.value
})
```
In addition, I tried deleting the `.value` because I didn't give a value for the score. 
When I refresh it, it worked!
``` JS
player.collides('egg', (e) => {
  destroy(e)
  score++
  scoreLabel.text = score
})
```

### Skills

Some skills I learned is collaboration, how to learn, and debugging. When me and my partner were creating the score board, we were planning out the number of points everytime the sprite collides with the food as well as how to make the score appear on the game. In addition, during this project, I was looking at tutorials and kaboomjs.com to see why my code was not working as well as learning new things. When builidng our MVP for our project, we were tinkering with the code and trying new things to see what will happen. 

### EDP

Last blog, I was on stage 3, 4, and 5. This blog, I am currently on stage 5, create a protoype and stage 6, test and evaluate the protoype. These few weeks, me and my partner were continuing on our MVP for our adventure game. In addition, we created the level, score, and make the sprite move and collide. When we finish each level, we try the game to see if it was working. 


[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)