---
layout: post
title:  "Game Changing"
date:   2017-10-16
categories: progress
---
# Monday....

Ugh, I feel like shit. The plague has struck with hateful vengence. 

Coding is not going well. It's a struggle. My mind is not handling cold meds super great. 

Alas! I have been able to do a decent amount of forward thinking on the course. There are times where I need to follow the course "code along" verbatim, but for the most part I find myself pausing, jumping ahead, and confirming my thoughts...or at least mostly. It's harder to "follow" this way since variables used in the code-along are different than the ones I choose, but for the most part it's working pretty well. 

I've also been getting in the habit of attempting to refactor prior to the course prompts

So, the course has us working on this (us? I don't know if that's propper...I mean...a bunch of people have taken it...and there is a community, but I am taking it by myself? who knows.).

It's a game where you are presented with 6 (or 3) tiles and an RGB value and you try to pick the right color value.

The "app" is covered over 9 videos...and I'm up to 6...so 4 more videos to complete. (I can maths...I havn't started 6 yet...so 6, 7, 8, 9)

most of the functionality is there...minus the  switching between "easy" and "hard" mode...so I'm assuming a lot of it will be about styling. Tempted to style it on my own..but might way...who knows.

![Color Game Day 1](https://github.com/Cybnew/myprogress/blob/master/assets/cpgd1.JPG?raw=true)

``` 
var colors = generateRandomColors(6);
var headerIdColor = document.querySelector("#headerIdColor");
var square = document.querySelectorAll(".square");
var pickedColor = pickColor();
var body = document.getElementsByTagName("body");
var bgColor = "#232323";
var guessText = document.querySelector("#guess");
var header = document.querySelector(".header");
var newColors = document.querySelector("#newColors");

newColors.addEventListener("click", reset);


headerIdColor.innerHTML = pickedColor;
colorTiles();

function colorTiles(){
	for (var i = 0; i < square.length; i++) {
	square[i].style.backgroundColor = colors[i];

	square[i].addEventListener("click", makeInvisible); 
	}

}


function makeInvisible(){
		//grab color of clicked square
		var clickedColor = this.style.backgroundColor; 
		//compare color to pickedColor
		if(clickedColor != pickedColor){
			this.style.backgroundColor = bgColor
			guessText.innerHTML = "Try Again"
		}else{
			header.style.backgroundColor = pickedColor
			guessText.innerHTML = "That's Correct!!!!"
				for (var i = 0; i < square.length; i++){
					square[i].style.backgroundColor = pickedColor;
					newColors.textContent = "Play Again"

				}
		}
}
```

Will post more tomorrow...brain is fried.


-Mat