# Entry 1 (Deciding and Tinkering my tool)
##### 11/7/2022

The tool I am going to use for my Freedom Project is Kaboom. In addition, my Freedom Project topic is making a adventure game. In the beginning, when I was trying to decide on what tool I am going to use for my freedom project, I wanted to use Three.js and Kaboom.js. 

First, I started tinkering with Three.js. Three.js helps create 3D designs that was really cool and interesting. When I was tinkering with Three.js, I learned about AmbientLight. AmbientLight helps give the same amount of light to all object. 
You can use `const light = new THREE.AmbientLight( color );` and `scene.add( light );` 
 ``` JS
 const light = new THREE.AmbientLight( #C2B4F5 ); 
scene.add( light );
```
When deciding on the color for the AmbientLight, you can use hexadecimal, RGB, and HSL.

After I finish tinkering with Three.js, I started tinkering with Kaboom. Kaboom helps make 2D games that was also really cool and interesting. In addition, the "PlayGround" in Kaboom gave me inspiration to create a game myself. There are different types of things like sprite, rpg, and level, where you can try out the game and see the code for making the game. When I was learning Kaboom, I really enjoy learning addlevel. In addlevel, you can use symbols to draw the outline of what you want the map of the level to look like.  
``` JS
addLevel([
    "                           ",
    "                           ",
    "           **             $",
    "  .      ====              ",
    "                      -    ",
    "       ==        =    -    ",
    "===========================",
], 
``` 
When the map in addLevel is finished, we need to define the symbol using `"symbol" : () => []`
``` JS
"=": () => [
        sprite("blue block"),
        solid();
    ]
 ```
 I found it really cool to see that the "=" actually turns into a blue block. 

 When I finish tinkering with both tool, Kaboom and Three,js. It was time to decide on the tool I am going to use for my Freedom project. I decided to use Kaboom because I wanted to make a adventure game that has many levels. 

### EDP
I am at stage 1, defining the problem and stage 2, researching the problem. These few weeks, I was deciding on what I want my project to be. I plan out different ideas about what kind of games I want to make for my freedom project. In addition, I started tinkering with my tool, Kaboom and Three.js. I looked at different tutorials and docs. After tinkering with my tool, I started to decide what tool I am going to use for my Freedom Project.

### Skills
Some skills I learned when deciding on my tool and my freedom project topic is How to learn, creativity, and embracing failure. One skills I learned is How to learn because when I was tinkering with my tool, I was trying out the code to see if it works and changing some of the codes to see what will happen if I change it. In addition, another skill I learned is creativity because when I was deciding on my freedom project topic, I drew out different pictures and wrote down different ideas for my game. Moreover, another skill I learned is embracing failure because when I was putting the CDN to my replit and code.cs50.io, it wasn't working. I kept trying to put the CDN in different places and watched tutorials and it worked! 

Link to Kaboom.js --> https://kaboomjs.com/ 

[Next](entry02.md)

[Home](../README.md)