# Entry 4 (Building my MVP)
##### 3/13/23

### Context
These few days, me and my partner was building and planning out our mvp for our adventure game. We wanted to make a food adventure game, where the sprite finds all the ingredients for the food to complete the level. In this blog, I will walk through my process on planning my MVP as well as building my MVP.

### Planning 
In the beginning, me and partner decided to plan out all the sprite, background and blocks before starting to build the MVP. 
* In the first level, we decided to create a cute background, where the sprite needs to escape from all the wishing glass through finding all the ingredients of a pizza. 

* Ingredients (Pizza)
    * Bread
    * Tomato Sauce 
    * Cheese
    * Menu 

![IMG_3620](https://user-images.githubusercontent.com/91750609/226145474-27511365-5e5f-4d21-86a9-1c9263eadb9f.jpg)


* In the second level, we decided to create a dark background, where the sprite needs to escape from the Queen of spiders through finding all the ingredients of a cake. 

* Ingredients (Cake)
    * Flour 
    * Egg
    * Sugar 
    * Frosting 
    * Menu

![IMG_3619](https://user-images.githubusercontent.com/91750609/226145479-87817f75-103b-4125-a501-ccfff63c2fd3.jpg)

### Building our game (MVP)

* When me and my partner started building the MVP for our adventure game, we decided to build both level first before making it interactive. We first create the background and blocks by drawing out all the images. 

* Levels 1 and 2 
    * We first load all the sprite for level 1 and 2 
```JS
//Loading the Sprite
loadSprite("background2", "img/background2.png"); // bakcground2
loadSprite("block", "img/block.png"); // block
```
<img width="70" alt="block" src="https://user-images.githubusercontent.com/91750609/226153521-1141f78b-6bae-4678-9153-df53572bb429.png">

```JS 
loadSprite("egg", "img/egg.png"); // egg
```
<img width="54" alt="egg" src="https://user-images.githubusercontent.com/91750609/226153531-49aa0ffe-4281-4e0d-8b2b-ae35663cc8e3.png">

```JS
loadSprite("cheese", "img/cheese.png"); // cheese
```
<img width="60" alt="cheese" src="https://user-images.githubusercontent.com/91750609/226153533-a207cfea-d1f4-4856-a4c2-a89ba22c62f3.png">

```JS
loadSprite("flour", "img/flour.png"); // flour
```
<img width="79" alt="flour" src="https://user-images.githubusercontent.com/91750609/226153539-6d75af7d-023b-4ace-9596-d1a2f83e8f40.png">

```JS
loadSprite("tomato", "img/tomato.png"); // tomato
```
<img width="48" alt="tomato" src="https://user-images.githubusercontent.com/91750609/226153540-eb42273e-590b-4f7f-a132-3b25b3b78589.png">


* After we finish loading all the sprite, we created a background for level 2.
```JS
add ([
sprite("background2", {width: width()), height: height())}) // background for level 2
])
```
<img width="446" alt="background2" src="https://user-images.githubusercontent.com/91750609/226153545-9448cf75-d73c-4f31-beb4-30e213a724df.png">

In addition, we also created a level for level 2
* In the beginning, we first created a small level to see if it works 
```JS
const level = addLevel (LEVELS[levelIdx]){ 
"=======",
], {
	width: 64,
	height: 64,

	"=": () => [
		sprite("block"),
		area(),
		solid(),
		origin("bot"),
}
```
When I preview it, it wasn't working.
<img width="1437" alt="Screen Shot 2023-03-18 at 11 16 34 PM" src="https://user-images.githubusercontent.com/91750609/226153554-83ac03f0-a92c-4d64-b77f-9f6672990e69.png">

In the beginning, I was confused what I did wrong. In addition, I tried to look at examples of what `levelIdx` is. In addition, I learned that `levelIdx` are argument in a scene. 
In addition, I tried creating a scene for my level and it worked! 
``` JS
scene("game", ({levelIdx}) => {
const level = addLevel (LEVELS[levelIdx]){ 
"=======",
], {
	width: 64,
	height: 64,

	"=": () => [
		sprite("block"),
		area(),
		solid(),
		origin("bot"),
    }
} 
```
### Skills 
Some skills I learned was debugging, collaboration, and creativity. During my journey in making my game, I learn debugging through finding my mistakes and learning from my mistake when I was making my level. In addition, another skill I learned is colloration. Me and my partner were working collaboratively in planning and building our MVP. In addition, I also learned creativity by planning out what background, sprite, and the type of game I want to make. 

### EDP
Last blog, I was on stage 2, research the problem. This blog, I am currently on stage 3, brainstorm possible solutions, stage 4, plan the most promising solution, and stage 5, creating a protoype. These few weeks, me and my partner was planning our MVP for our adventure game. In addition, me and partner also started builidng the levels for our MVP. 


[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)
