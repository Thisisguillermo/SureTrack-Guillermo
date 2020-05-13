# Learning programming advice.

# Software design pattern

https://www.wikiwand.com/en/Software_design_pattern

Look for the books.


# https://dev.to/jessicajades/20-tips-for-learning-to-code-in-2020-341i
https://dev.to/jessicajades/20-tips-for-learning-to-code-in-2020-341i

# Experiences

Actually before writing a program, if you have no clue how to start, this is what I do (idk if it works for others but I do it this way)
First you sketch the thing out. Like visually. What you can see as a user.
Then you go in one level at a time. What data structure you need? What maths you need to do?
The data structure part is very important, and is very often overlooked by new programmers.
You get that wrong, and you'll end up rewriting your thing when you want to do something but your current structure says no.
Like, you want to build a pong game (or whatever that is called)
So first, you need a board to draw your things.
Then, you need two plates. They needs to be controlled.
Then you want to know where the plates are so that you can know if the ball should bounce off them or should hit the edge and end the game
So naturally, you need the coordinates in a data structure that you can associate with the plates.
Or in the plates itself, if you make it into a class (I'll almost make everything into classes... that's a habit after learning C++)
Most of the time you'll be spending on is to tinker around on how you want to tear down your program's bits and determine what each part should have, and how parts should be related to each other (x calls y, y reads from z, etc). After that it's just a matter of flex taping them up correctly and boom, it works.
(Hopefully, otherwise have fun debugging but it's going to be fine assuming that your data structure is correct for your plan)
And yeah, use a notebook if your program is slightly big. It helps. And don't worry if you find yourself repeating the structure designing phase because it's always like this.


Umm well I follow this method when it comes to make the code do what I want it to - (I only use it in big stuff because it is also like a mind map)

1) Think about the program in depth
2) Think about the methods
3) Write a pseudo code
4) Start fucking writing the code

In the Python world I've heard good things about http://www.openbookproject.net/thinkcs/python/english3e/

You know when I started, I watched Sentdex's Python tutorials in which he taught beginner concepts by teaching you how to make a complex tic-tac-toe

A lot of programming revolves around the mindset and problem solving, so going through at least one thorough programming book / guide will help you a lot in being able to tackle a full scale project

That's not cheating to be honest
When you are at the early stage of learning then you require these kind of beginner projects
Remember when you were learning poems in kindergarten? Did you make your own poems or first learn the poems made by others?
And when it comes to programming, the search engine is your best friend and sites like Stack Overflow are your girlfriend (s)
When it comes to videos (as you asked), I like the ones made by Sentdex and thenewboston
As for the books, I read - Sam Teaches C in 21 days, Learning Python 5ed by Mark Lutz, Python Cookbook 3ed etc
And for the something part you asked - Try reading source codes to build up understanding about what the program does (tbh, I suck at it) and solve some cool short problem which are available on the internet.

it takes time to get used to thinking algorithmically and reading example code will of course be much easier than writing it at first
But there's no way around using tutorials, books, etc.
Ideas for projects will come naturally as you think of things that bother you that you think you can automate.

I recommend new coders don't copy/paste code but actually re-type it line by line. To me, that helps you to notice each symbol, character, etc. Plus, you'll make typos which is a good introduction to debugging. (See an error, figure out the line it refers to, compare your code to their code).  I remember stuff better if I read->write vs just read/copying n lines at once.

There's a difference between "copy pasting" and "looking up something on stackoverflow, understanding what it does, and retyping it / reimplementing it in your code"
Besides, a significant amount of develops do tend to copy tidbits of code here and there
There's no need to reinvent the wheel everytime you do something.

Try python first it's a lil bit easy to program in it
It's more beginner friendly


This too: https://www.khanacademy.org/computing/computer-science

If you want to eventually work with nodejs, my advice would be to stick to chrome/chromium because you are likely going to run into information about the internals, which is how V8 operates. And then you can apply that knowledge in the browser as well as with Nodejs

---

https://www.youtube.com/watch?v=WgsdpJSyqc0&list=WL&index=4&t=0s

https://www.reddit.com/r/learnprogramming/comments/fx884k/read_practice_tutorials_think_i_understand_get_to/

https://news.ycombinator.com/item?id=22960225

https://www.reddit.com/r/learnpython/comments/ggd2lz/noob_rant_am_i_really_supposed_to_just_know_how/

---

Part of learning to program is learning how to think and learning how to solve problems. Don't concentrate just on learning a language.

I say this because I'm only just past the tictactoe lab at 38 years old with no prior programming.

So... Take it step by step.

How could we, at that module, represent a 3x3 grid numbered 1 to 9? We could have individual variables for each box. We could have a list 1-9 (or 0-9 in python parlance) We could a list of 3 numbers representing rows and each entry in the list could have a list of 3 numbers. 3*3=9.

It doesn't really matter which you choose, but some are more elegant and some use fewer lines of code or fewer variable names to remember, which could be a factor if your program ends up being bigger.

Okay, so now we need to think how to talk to each box. Either variable name or an index like board[1][2]

Then we tackle hoe to check what a box currently contains, and how to change what a box contains depending on an action. So if board[1][2] == "X": user_input().

Then we figure out to allow a player to choose their turn, check that it's a valid input, check that that box is available, and check it that move results in a win, loss or draw.

Then we figure out how to make the computer take a turn. I used a random integer generator (Google), but you could just make the computer start in the middle box then subsequently move into the first available box starting at 1.

Then before you know you have achieved the labs aim, but can think of ways to make it better, and have grand plans about training a machine learning algorithm to beat human players!!

Congrats - you've learned how to think. And I genuinely don't mean that condescendingly - thinking like this IS a learned skill and it more important than the language you choose to learn.

---

a large part of it is breaking down the problem into smaller problems

for tic tac toe i see a few key parts:

1 : board structure - how would you model a board in code?

2 : move legality - only allow the move if the tile hasn't been used already

3 : checking for a win - check if any row, column or diagonal contains one type of player input (X or O)

see how each of these problems are individually much smaller than tic tac toe as a whole? once you've got these, you just need to glue them together with a turn counter that alternates the users after they make their moves

try implementing the steps above and see what you come up with

also don't be afraid to look at how other people did things. just imagine if in school you weren't taught how to do algebra and were expected to just know it. the best way to learn is by seeing how similar problems are solved and then applying it to your own

just don't copy code line for line, make sure you actually understand how it works and try to take inspiration from others

When I first learned a programming language, it was from a book. I did all the exercises, all the bonus assignments, totally understood what was going on. Then I finished the book and wanted to start on something of my own

Besides having trouble coming up with an idea, I felt like I would hit a road block almost immediately after trying anything. There was all this stuff I thought I knew how to use, but when I tried to make it work on my own, it just didn't. I remember almost feeling like the computer was making things difficult for me on purpose or something.

I think it's like that for a lot of people. It's a big shift in mental gears to go from following along with a pre-planned tutorial, to just coming up with your own goal, knowing what kinds of commands are available, and how to piece them together to behave a certain way.

That's something that can't be taught, but needs to be learned. So that's where you are right now. Be patient with yourself, and learn from your upcoming discoveries.

Programming is about figuring out how to make this stuff work. It's what all of us are doing, just at different levels. I wouldn't be able to just sit down and write a tic tac toe program from start to finish. It would probably take me a couple of starts, several major structural changes, and lots of googling things for docs or guides.

Yes, people can do these things from scratch. But only after practice. I suspect you might be similar to me, and need to work backwards from a problem. Find a problem you're interested in solving, then look for the tools you need to solve it.
level 2
skellious
DollarStarNova1 point ·
4 minutes ago

exactly. it's like the pavement artist who draws a caricature in 5 minutes and then the customer says "I'm not paying you $20 for that, it only took you 5 minutes!"

"yes, it only took me 5 minutes to draw that, but it took me 12 YEARS to learn HOW to draw that in 5 minutes."\

---

Step one: come up with a simple problem. Start really simple.

Step two: write out every step to solve it, in English.

Step three: turn what you wrote into a bunch of comments. After each step’s comment, write just enough code to do that step.

The thing people forget is if you don’t know what you want to do well enough to say it in English, you’re not going to be able to write the code! Plus this approach helps with the “staring at an empty page” thing.

In addition you probably should get some kind of book aimed at beginners, as well as watching videos. I like the books on invent with python, they are also free which is a nice bonus. The book on inventing games with python would be a good pick. Don’t just read it, type in the programs, that step is essential.

https://www.reddit.com/r/learnprogramming/comments/ghowzp/how_do_i_create_code_as_a_beginner_instead_of/