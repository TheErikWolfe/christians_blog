---
layout: "post"
title: "First Post, Let's talk style"
---

## The moment you have been waiting for.. Whether you knew it or not.
	
Before I get into what this post is about let me say that this blog is brought to you by Awesome Inc U. With the guidance of a few well trained instructors I am slowly but surely learning my way around web programming. The class has taken off **fast** and I am running with two left feet but I am still keeping up. All this to be said, please be patient as I continue to make mistakes with html and css. More importantly, if something bothers you please don't be afraid to provide feedback. So, without further to do, enjoy my very first blog post!
		

## Consistent Styling. Por Que?

Something that I have always tried to pay attention to in anything I do is consistency. Whether it is in my daily schedule or writing notes in a class. However, I find that as I am going through this programming bootcamp that people may not know the importance of indentation or general program organization.
				
When you start programming the first and only thing you are looking to do is make any program you write work. How your code looks when you are done is always the last thing on a new programmers mind and is often never revised. It can often be seen as "If it works, why does it matter?". I look back on some of my earlier programs now and think "What in the world was I smoking". 
		

## So why does it matter?
	
When you are writing a program the compiler will often accept anything as long as the semi-colons are in the right place and there are no syntax errors. In small programs the indentation or stylistic choices hardly seem important because even if it is hard-ish to read pretty soon you will have the program completed and you won't have to think about it again. 
		
	
Now, imagine a program that is starting to get upwards of a thousance lines where standards aren't followed for style or indentations. Your code looks like a free for all and the winner is unclear. When you try to look back at it to fix a bug you can't tell a for loop from a function. So you inevitably give up and think to yourself "WHY OH WHY DIDN'T I HEAD CHRISTIANS WRANING!!"
		
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
for(var i = 0; i < x; i++)
{
if(i == 3)
{
x++;
}
}
}
```
#### With Odd Indentation
```
function code(x)
{
	for(var i = 0; i < x; i++)
	{
	if(i == 3)
	{
	x++;
}
	}
}
```
#### With Indentation
```
function code(x)
{
	for(var i = 0; i < x; i++)
	{
		if(i == 3)
		{
			x++;
		}
	}
}
```

Between the two I think we can all say it is easier to read the second.


Last thing I'll say about indentation is that **I** strongly prefer for the curly brackets to line up. I can't say this is a general standard because it varies between programmers. When some porgrammers write a function the put the first curly bracket on the same line as the declaration of the function. Others will make sure the curly bracket is on the next line and the closing curly bracket will line up with it. I don't care what you do and I can read it either way but no matter what, **BE CONSISTENT!** I've provided two examples to show you the difference.


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


The same crazy concepts can be applied to html, css, xml, or any other computer language. 
		
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
# Style With Line Breaks		 
The other important thing when you are coding is style. When you are reading a program that looks like gibberish it is often easier to read if there are stylistic choices done to it. For instance, adding line breaks between groupings of code. The compiler doesn't need the line breaks and will just read over them but people do. The choice of when to add a line break is entirely up to the programmer but to many breaks in too many places can lead to the same amount of confusion as no line breaks. I *personally* will add lines after groupings of variables, after functions and for loops, and when I feel like the next line of code doesn't need to be organized with the previous. If I am making a series of if/else if/else statements I will keep them clumped together but will add line breaks inside of them. So far instance
		

#### With Line Breaks
```
function code(x)
{
	var x = 0;
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
function code(x)
{
	var x = 0;
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
		
## This is Where You Thank Me

In conclusion even though these things may feel basic, they are **EXTREMELY** important tools as a programmer. Your code may not always be just yours and just like with your handwriting, you don't want to write sloppy in case you or anyone else needs to come back and re-read your code. So remember, consistency is key for anything you write, and if you are confused when reading your code, it will be confusing to others to! 

Alright folks, good luck with your programming and be careful out among them English.