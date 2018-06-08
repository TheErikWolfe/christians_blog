---
layout: "post"
title: "Technical Styling, Part 1"
---

Hi! Welcome back! How's it going? Me? I'm fine. Okay, enough small talk.

Today I'd like to branch off from what I wrote about last week and talk about very common practices to keep your code clear, concise, and easy to traverse. It will all be very simple stuff and I might repeat some things from my first blog but it doesn't decrease the value of it's importance! So as I'll often say, let's get into this.

## Why it is important

First and foremost, let me tell you why it is *important*. I promise I am not a code nazi, I just know how much time you can poor into bad code and how dificult it can be to traverse it. More importantly, I might save you from the headache of having to figure out how to slug through bad code. 

When in college, I had to learn this the hard way. My teachers let me loose to write horrendous code and didn't teach me proper coding. It wasn't until I was in the thick of it that I was told that "programming isn't hard, you're just a bad programmer". Harsh words, I know, but that's okay. An injured pride can lead a man to do incredible things. After being told that I made it my goal to write pretty code and to always strive for efficiency.

One more thing I'll say about why it is important. The code you write won't always just hide inside your laptop, never to see the light of day again. It might need to be used for a professional website or app and it will be seen and used by more than just you. One of the best pieces of advice I have **EVER** heard was from one of my professors who said "your code is like a diamond, it last's forever". After he briefly told a story about one of his first programs he wrote, about 20 years ago, for a university. He said that not only was that program the *worst* program he has ever written stylistically, but it is still used today as a building block for a larger program. Wow, okay, that's crazy. Imagine a program you have written poorly being used as a building block. That's when you wish you had practiced good techniques sooner!

## Putting the Fun in Functions

Let's talk first about writing functions. I will do all my code demonstrations in javascript but the same principles apply to all programming languages. When you are first writing a program you might have some pseudo code or an idea of what your program is to look like, but you may not know exactly what when to write a new function for a section of code. 

Figuring out when to write a new function or when to keep working in the old can be described in 3 simple rules:

1) If you repeat a block of code more than once, it would be better to write a function.
2) If the block of code you have written makes your function look cluttered it would be better to write a new function.
3) Just like a sentence, if it finishes a thought, finish that function and section off the next thought in a new function.

So, what does this mean? Well it will be easier for me to show you then to just expect you to understand.

### Rule 1:
Let's say you have a program where you are writing a block of code where you are updating a series of html elements.

```
var q = 1;

function displayTaco() 
{
	taco.style.display = 'block';
    burrito.style.display = 'none';
    enchilada.style.display = 'none';
}

function displayBurrito() 
{
    taco.style.display = 'none';
    burrito.style.display = 'block';
    enchilada.style.display = 'none';
}

function displayEnchilada() 
{
    taco.style.display = 'none';
    burrito.style.display = 'none';
    enchilada.style.display = 'block';
}

if(q = 1)
{
	displayTaco();
}
else if(q = 2)
{
	displayBurrito();
}
else
{
	displayEnchilada();
}
```

When displayed it will will display the taco block in the html. When you look at this there is nothing wrong with the code practically, but as you can see it is repetitive. This is when Rule 1 can be applied! So we go from that to this:

```
var q = 1;

function displayMexicanFood(tacoDisp, burritoDisp, enchiladaDisp) 
{
    taco.style.display = tacoDisp;
    burrito.style.display = burritoDisp;
    enchilada.style.display = enchiladaDisp;
}

if(q = 1)
{
	displayMexicanFood('block', 'none', 'none');
}
else if(q = 2)
{
	displayMexicanFood('none', 'block', 'none');
}
else
{
	displayMexicanFood('none', 'none', 'block');
}
```

**BOOM**! Just took 10 lines of code out of this program right before your very eyes! Okay, it may not seem that crazy. Let's say you added a new element, quesoAndChips.style.display, now you only have to call that one function with the parameters for quesoAndChips instead of writing a whole new function for it.

Rule 1 doesn't only apply to condensing functions into one. If you find you have written the same line or block of code in more than one area in your program just go ahead and write a new function for it. It is as simple as that.

### Rule 2:
Okay, I admit, I like pretty code. I might actually be a little crazy about it. I can feel myself breaking into cold sweats and feeling ill when I see code that is ugly. So that's where this second rule comes from. Organizing your code, just like stylizing it, can take your program from 0 to 60. It can make it easier to read and can help you and others skip over the unimportant parts. 

For Instance, just the other day I wrote a chunk of code that could've cluttered a function to the point of confusion. With my quick wit I knew it called for a separate function. Let me show you what it could've been and what it turned out to be.

```
function displayMenuItems(item)
{
	var node = menuItem.cloneNode(true);
	var cloneNodeAttributes = node.querySelector('[id="menuItemTitle"]');
	cloneNodeAttributes.innerHTML = item;

	var cloneNodeImg = node.querySelector('[id="menuItemImg"]');

	var foodImg = '';

	if(item.indexOf('beef patty') != -1)
	{
		pic="beef-patty.jpg";
	}
	else if(item.indexOf('beef ribs') != -1)
	{
		pic="beef-ribs.jpg";
	}
	else if(item.indexOf('chicken leg') != -1)
	{
		pic="chicken-leg.jpg";
	}
	else if(item.indexOf('omelet') != -1)
	{
		pic="omelet.jpg";
	}
	else
	{
		pic='trash.jpg';
	}

	cloneNodeImg.src= './images/' + foodImg;

	node.style.display = 'block';
	menu.appendChild(node);
}
```

With the massive if/else chain I made, I split the function in half. If I wanted to look at the function I would have to scroll up to see the top part and then scroll down to see the bottom. Enter new function stage left.

```
function getPic(item)
{
	var pic;
	if(item.indexOf('beef patty') != -1)
	{
		pic="beef-patty.jpg";
	}
	else if(item.indexOf('beef ribs') != -1)
	{
		pic="beef-ribs.jpg";
	}
	else if(item.indexOf('chicken leg') != -1)
	{
		pic="chicken-leg.jpg";
	}
	else if(item.indexOf('omelet') != -1)
	{
		pic="omelet.jpg";
	}
	else
	{
		pic='trash.jpg';
	}
	return pic;
}


function displayMenuItems(item)
{
	var node = menuItem.cloneNode(true);
	var cloneNodeAttributes = node.querySelector('[id="menuItemTitle"]');
	cloneNodeAttributes.innerHTML = item;

	var cloneNodeImg = node.querySelector('[id="menuItemImg"]');
	cloneNodeImg.src= './images/' + getPic(item);

	node.style.display = 'block';
	menu.appendChild(node);
}
```

Wow, what a relief to be able to skip that entire function and just see my block of code with no if/else monster. All kidding aside, I hope you can see and why this might be important. 

### Rule 3:
With some programs you can write your entire program in one function. With some programs when I was using c++ I would just make the entire program in ```int main() {}```. I was so *foolish*, so *young*, so *naive*... 

Like I said before, finish a function like you finish a sentence; when the thought is over. What does this mean? Your functions should only do what they need to, and never more than that. If you find your function is divided by a giant if/else statement comparing two totally different things you probably should've made a different function. If you find that a part of your function is called several times and you have to skip the first part of the function to use it, make a new function. This may be the part that is hardest to explain in code but I'm going to try anyways with a small example.

```
function saveMenuItems(check) {
	if(check)
	{
		list = apiRequest.responseText;

		localStorage.setItem('menu', JSON.stringify(list));
		loadMenuItems();
	}
	else
	{
		var list = JSON.parse(localStorage.getItem('menu'));
		if (list == null) 
		{
			getMenuItems();
		}
		else
		{
			menuItemTitle.innerHtml = '';
			list = JSON.parse(list);
			for(var i = 0; i < list.menu_size; i++)
			{
				displayMenuItems(list.menu_items[i].description);
			}
		}
}
```

See how the if statement is passing in a boolean called check to see if we should be saving or loading? Well I would argue that saving is a thought, and loading is a separate thought, and they should be treated as such. So instead of having a metaphorical run on sentence it is better to just split them up.

```
function saveMenuItems() {
	list = apiRequest.responseText;

	localStorage.setItem('menu', JSON.stringify(list));
	loadMenuItems();
}

function loadMenuItems()
{
	var list = JSON.parse(localStorage.getItem('menu'));
	if (list == null) 
	{
		getMenuItems();
	}
	else
	{
		menuItemTitle.innerHtml = '';
		list = JSON.parse(list);
		for(var i = 0; i < list.menu_size; i++)
		{
			displayMenuItems(list.menu_items[i].description);
		}
	}
}
```

## [Get On With It](https://youtu.be/l1YmS_VDvMY)

I know I kinda carried this on a bit, so please forgive me. Regardless of my rambling, these things are important, and they may just save your life one day. So I'm going to step off my soap box for now but when I step back up next week we can talk about when to use for loops and if statement! ***Woohoo***! Until then, have a good day and you be careful out among them English. 

TTFN. Ta ta for now. 