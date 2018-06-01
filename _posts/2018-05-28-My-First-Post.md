---
layout: "post"
title: "First Post, Let's talk style"
---

## The moment you have been waiting for.. Whether you knew it or not.
	
Before I get into what this post is about let me say that this blog is brought to you by Awesome Inc U. With the guidance of a few well trained instructors I am quickly learning my way around web programming. The class has taken off **fast** and sometimes I feel like I am running with two left feet, but I'm still keeping up! All this to be said, please be patient if I make mistakes in these blogs. More importantly, if something bothers you please don't be afraid to provide feedback. So, without further to do, enjoy my very first blog post!
		

## Consistent Styling. Por Que?

Something that I have always tried to pay attention to in anything I do is consistency. Whether it is in my daily schedule or writing notes in a class. However, I find that as I am going through this programming bootcamp that people may not know the importance of indentation or general program organization.
				
When you start programming the first and only thing you are looking to do is make any program you write work. How your code looks when you are done is always the last thing on a new programmers mind and is often never revised. It can often be seen as "If it works, why does it matter?". I look back on some of my earlier programs now and shutter at the things I did/wrote.
		

## So why does it matter?
	
When you are writing a program the compiler will often accept anything as long as the semi-colons are in the right place and there are no syntax errors. You could write an entire program on a single line and the compiler won't even know the difference. In small programs the indentation or stylistic choices hardly seem important because even if it is hard-ish to read pretty soon you will have the program completed and you won't have to think about it again. 		

Here is my warning:
**DON'T DO THIS! START STYLISTIC PROGRAMMING NOW WHEN IT DOESN'T COUNT, SO WHEN IT DOES COUNT YOU ARE ALREADY DOING IT!**

Now, imagine a program that is starting to get upwards of a thousand lines where standards aren't followed for style or indentations. Your code looks like a free for all and the winner is unclear. When you try to look back at it to fix a bug you can't tell a for loop from a function. So you inevitably give up and think to yourself "WHY OH WHY DIDN'T I HEED CHRISTIANS WARNINGS!!"
		
So let's get into this.
		

## Tabbing/Indentation
Whether you understand the code in this section or not you should pay attention to how neat it looks when it is properly indented.
		
Indentation is very easy to understand. As far as I can tell there are two simple rules.
		

-Everything in a function is indented once
-Everything in a for/while/if statement is indented once

	
Sounds easy, right? It's because it is. But you wouldn't believe the number of new programmers who can't seem to figure it out. Let's take a look at a piece of code written without indentation, with odd indentation (which seems exagerated but happens all the time), and with correct indentation.
		

#### Without Indentation
```
function code(x)
{
var num = 0;
for(var i = 0; i < x; i++)
{
if(i == 3)
{
num++;
}
}
}
```
#### With Odd Indentation
```
function code(x)
{
var nume = 0;
	for(var i = 0; i < x; i++)
		{
	if(i == 3)
	{
	num++;
}
	}
}
```
#### With Indentation
```
function code(x)
{
	var num = 0;
	for(var i = 0; i < x; i++)
	{
		if(i == 3)
		{
			num++;
		}
	}
}
```

Between the three I think we can all say it is easier to read the third.


Last thing I'll say about indentation is that **I** strongly prefer for the curly brackets to line up. I can't say this is a general standard because it varies between programmers. When some porgrammers write a function they put the first curly bracket on the same line as the declaration of the function. Others will make sure the curly bracket is on the next line and the closing curly bracket will line up with it. I don't care what you do and most people can read it either way but no matter what, **BE CONSISTENT!** I've provided two examples to show you the difference.


#### Same Line Curly Bracket
```
function code(x) {
	var = "Javascript is Great!";
}
```

#### Next Line Curly Bracket

```
function code(x) 
{
	var = "Javascript is Great!";
}
```

With this said, you might prefer one thing stylistically in one language and something else in another language. For instance, when writing in javascript, c++, java, or PHP, I love making my curly brackets line up. But in css I think it is stylistically cleaner to have the same line curly bracket. So, don't be afraid to change it up depending on your needs or preferences.


The same crazy concepts can be applied to html, css, xml, or any other computer language. For instance with HTML:
		
```
<html>
	<head>
		<title>Awesome</title>
	</head>
	<body>
		<h1>This is a Header</h1>
		<p>
			Awesome paragraph can be indented b/t p tags
		</p>
	</body>
</html>
```
## Style With Line Breaks		 
The other important thing when you are coding is style. When you are reading a program that looks like gibberish it is often easier to read if there are some stylistic choices done to it. For instance, adding line breaks between groupings of code. The compiler doesn't need the line breaks and will just read over them but people do. The choice of when to add a line break is entirely up to the programmer but to many breaks in too many places can lead to the same amount of confusion as no line breaks. I *personally* will add lines after groupings of variables, after functions and for loops, and when I feel like the next line of code doesn't need to be organized with the previous. If I am making a series of if/else if/else statements I will keep them clumped together but will add line breaks inside of them. So, for instance:
		

#### With Line Breaks
```
function code()
{
	var x = 10;
	var y = 0;

	for(var i = 0; i < x; i++)
	{
		if(i == 3)
		{
			x++;
		}
		else if(i == 4)
		{
			x++;
		}
		else
		{
			x--;
		}
	}

	var stringThing = "This is a string";

	return stringThing;
}
```
#### Without Line Breaks
```
function code()
{
	var x = 10;
	var y = 0;
	for(var i = 0; i < x; i++)
	{
		if(i == 3)
		{
			x++;
		}
		else if(i == 4)
		{
			x++;
		}
		else
		{
			x--;
		}
	}
	var stringThing = "This is a string";
	return stringThing;
}
```

Sure you can still read the second segment of code but compared to the first, it just doesn't feel as approachable.
		
## Style with spacing
The same idea with line breaks can be applied to spacing. Often you can clump together variables with operators and not worry about it, but it isn't always easy to read. I will often add spaces before and after operators, and after semi-colons and commas. I will not add spaces after periods when combining functions to variables though. As always, an example folllows.

```
function x(B)
{
	var D=10;
	B=B.Number();
	
	for(var i=0;i<D;i++)
	{
		B=B+1;
	}

	if(B===D)
	{
		D=0;
	}

	return D;
}
```
```
function x(B)
{
	var D = 10;
	B = B.Number();

	for(var i = 0; i < D; i++)
	{
		B = B + 1;
	}

	if(B === D)
	{
		D = 0;
	}

	return D;
}
```
## Style With Comments
Here is the last, but maybe the most important, thing I will say about style. Labeling sections of code with comments will take your program from 0 to 60. When you have a grouping of variables that do a specific thing or keep track of elements that effect large portions of your program, labeling them with a comment and using comments to explain what is happening to a variable can help you easily traverse your program. Using comments to write "TODO:" can help you find the portions of code that you still need to complete or come back to. Not only that but when you are working in a group, having descriptive comments can help the next programmer pick up where you left off. I'm going to show an example from some code I wrote for a weather app with no comments and one with comments. I am not going to say my commenting is perfect but often I can find what I'm looking for by searching key words. One quick note before we get to the example, you can write bad comments too. Comments should describe exactly what is happening or describe what a clump of variables are. They should never use phrases like "do the thing" or "makes stuff happen". This is not helpful, so don't do that.
```
function catchResponse()
{
	if(apiRequest.statusText === "OK")
	{
		var response = JSON.parse(apiRequest.responseText);

		error.style.display = 'none';
		dayTime.innerHTML = getDate();
		cityState.innerHTML = response.name;
		weatherCondition.innerHTML = response.weather[0].main;
		kelvin = response.main.temp;

		displayImg(response.weather[0].id);

		output.style.display = 'block';
	}
	else
	{
		error.style.display = 'block';
		errorMessage.innerHTML = apiRequest.statusText;

	}
}
```
```
/*
	function catchResponse should:
	- Check to see if the status of the api request was good, if it was:
		-- Parse through the api request
		-- Hide The error block in my html
		-- display Time, City, Weather Condition, and Tempperature
		-- Call function displayImg to post an image in html block
		-- reveal the html block
	- Else:
		-- Reveal error block
		-- Display error message
*/
function catchResponse()
{	
	// Status Check
	if(apiRequest.statusText === "OK")
	{
		// Parse through the apiRequest
		var response = JSON.parse(apiRequest.responseText);

		// Display the correct html with city, time, weather condition, temperature in kelvin.
		error.style.display = 'none';
		dayTime.innerHTML = getDate();
		cityState.innerHTML = response.name;
		weatherCondition.innerHTML = response.weather[0].main;
		kelvin = response.main.temp;

		// Calls displayImg to display the image using id found in the API JSON Parse
		displayImg(response.weather[0].id);

		// Reveal block of html on webpage
		output.style.display = 'block';
	}
	else
	{
		// Reveal error block of html on webpage
		error.style.display = 'block';

		// Show error message retrieved from the apiRequest
		errorMessage.innerHTML = apiRequest.statusText;

	}
}
```

I know that the second chunk of code was longer than the first. However, if you were new to *my* program and read *my* comments as you were trying to figure out what *I* did, it would help **A LOT**. Even if I wasn't as thorough with my comments and just labeled groupings of variables, it would still be more helpful than trying to understand a program with no comments. If you don't plan on sharing your program it can still be useful to yourself. I often use my previous programs as references when I know I used a specific function. If I didn't have my comments in there I would have to parse through the code just to figure out where that function was used and how the value works with other parts of the program. A quick comment about that function and value can save me a lot of time. What I'm saying is, think of your future self, not of your current self.

## This is Where You Thank Me

In conclusion even though these things may feel basic, they are **EXTREMELY** important tools as a programmer. Your code may not always be only yours and, just like with your handwriting, you don't want to write sloppy in case you or anyone else needs to come back and re-read your code. So remember, consistency is key for anything you write, and if you are confused when reading your code, it will be confusing to others to! 

Alright folks, I'll step down from my soap box and pack up my picket signs. Good luck with your programming and be careful out among them English.