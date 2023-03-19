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


* In the second level, we decided to create a dark background, where the sprite needs to escape from the Queen of spiders through finding all the ingredients for a cake. 

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
image
loadSprite("egg", "img/egg.png"); // egg
image
loadSprite("cheese", "img/cheese.png"); // cheese
image
loadSprite("flour", "img/flour.png"); // flour
image 
loadSprite("tomato", "img/tomato.png"); // tomato
image

    * After we finish loading all the sprite, we created a background for level 2.
```JS
add ([
sprite("background2", {width: width()), height: height())}) // background for level 2
])
```
Image 
In addition, we also created a level for level 2
* In the beginning, we first created a small level to see if it works 
```JS
"@  ^ $$",
	"=======",
], {
	width: 64,
	height: 64,

	"=": () => [
		sprite("grass"),
		area(),
		solid(),
		origin("bot"),
```
When I preview it, it wasn't working.
``` JS 







### Skills 


### EDP



[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)
