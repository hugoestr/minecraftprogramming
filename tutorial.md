# Tutorial

# Content
0. Setting up the environment
1. Watch, Hack, and Learn
2. Again, and again, and Again
3. Tidying up with object
4. Reading code
5. The game loop
6. Knowing about the world

## Sequence of scripts
* block.py, 0, 1
* column.py 2
* moving.py 3
* scanning and mob.py 4
* follow.py and mob2.py 6
* tagging.py and weepingAngel.py 6

# Setting up the environment

If you are a kid, get an adult to help you out to set up the environment. If you have access to a tech meeting, get someone to help you. 

Often setting up programming environments can be tough and frustrating. But just because it is it shouldn't be the obstacle that stops you from learning programming.

You will be using notepad. But if you can, get notepad++. Even if you use none of the text editor features, just the syntax highlighting is super helpful.

# Watch, Hack, and Learn

## How we actually learn languages
Recently I found a story about how people actually learn other languages. People are exposed to the language, and the more exposed you are, the quicker your brain picks it up. But how about learning grammar and vocabulary? Well, it is fun, but it doesn't help one learn a language except that it is giving us more exposure to the language. Yet if you were in a hurry, it would be more useful to buy a few magazines of Italian and just attempt to read it than taking a course on it. Then looking up a word becomes meaningful because there is a sentence that you want to understand. 

I sense that the same is true about computer programming. While many of us have taken classes, the true learning happens when we are exposed to code. Programmers often just copy-and-paste and then change something from the code. With the patterns become known and automatic.

You may run into people saying derogetory things about copy-and-paste programmers. Don't listen to them. Everyone has learned this way, including the people critizing others. 

# The most important part of the book

The whole book can be summarized in the following manner. You are a scientist. You are a hacker. You are learning by trying things.

* Get code
* See what it does
* Change it
* See what it does

You will get errors. That is okay. It won't do what you think it does. That is okay as well. The point is that you should be learning something about the code or its behavior. 

You are allowed to break things. Nothing bad will happen. At least while you are a beginner.

If it bugs you that you don't know why something is working a certain way, then try to find out. And you will remember it better because there is a meaningful thing to do.

We will guide you on some exploring, explaning some concepts, and then giving you a challenge. On the challenge, get a timer and do try it for only 5 minutes. Then stop. The point of the challenge is to understand the problem. If you solved it, good. If you didn't, that is fine. Move on and learn the solution.

And just keep trying things. Feel free to repeat statements. Or change the values. 

## Have a goal in mind

Think of something cool that you want to do. If you have a goal, then coding is a lot more fun. Then learning specific things is very meaningful, and you will remember it.

That is why we are going to build a mob.

## Dig as deep on concepts as you wish
At some point we will introduce concepts such as "lists", "functions", or "objects." As long as you know enough about how they work, that is fine. Yet if you want to learn more about it feel free to learn. Go as deep as you want, but if you get confused for too long, stop and go back to coding. Don't get lost by the conceptual siren.


# Creating a block

On the console, run the following statement:

python block.py

Now check the server console. You should see some new lines of text talking about a script connecting and disconnecting. Now go back to minecraft. You should see a block right next to you. If you can find it, turn around. It will be a stone block.

So whenever you run a script, you should expect to see change in the server, and then something changing in minecraft. Only if there is a change in the server will you see a change in minecraft. Programmers call these changes output, so that is the term that we will use.

Open the code in the text editor. This is what creates a block. Read the code aloud. See if you can get an understanding of what it does. Read "=" as "becomes".  Make a short silence for periods. Don't say anything for the parentheses sysmbols.

[x,y,z] = world.player.getPos()

Would read like

x, y, z become world, player, getPos

world.setBlock(x+1, y, z+1, block.STONE) would read

world, setBlock exs plus one, y, ze plus one, block, stone

Now read the code aloud.

No, I really mean it. You must read that code allow. Do it. 

Did it make sense? Maybe not complete sense, but you should be able to understand that the code creates a minecraft world, finds the position of the player, and then sets a block to stone.

You will often have vague understanding about code. That is normal and fine. Sometimes you don't need more information, so you forget about it. But if you need to know what is going on, then we start experiments. Let's experiment and see what we learn form this code.

##Experiment 1

Steps: Erase the two lines that start with import. Now run the code

python block.py

What happens?

Nothing should have happened in Minecraft. Nothing should have happend in the sever console. And you should have seen an error message.

So what have we learned? We learned that two two lines are important. Put them back in. Run the script again. Now the block appears. So the script won't run uneless we have those two lines.

But why?

#### computers are dumb

Yes, computers are dumb. Very, very dumb. They only understand a certain amount of words, and they will only understand them if we tell them explicitely, "go and learn these words." A collection of words that the computer can understand are called libraries, modules, or dictionaries, depending on the language. Python calls them modules, so we will use that name.

The import command tells the python to look for the mcpi.minecraft library, once it finds it, it tells it, let's call it "minecraft" as a nickname. So the whole line reads

import (module) mcpi minecraft as (let's call it) minecraft
import (module) mcpi block as (let's call it) block

But where is the module? Look at the development folder. You will find a folder there called mcpi. Click on it. In there you will find a file called minecraft.py and block.py. Open the source code. This is the code that teaches the computer how to understand the words Minecraft.create(), setBlock(), and block.STONE. You won't understand it, and you don't need to understand it, but spend some time looking at the code. This is how things are put together.

## Experiment: let's use the full name

Change block.STONE to read mcpi.block. Run the code.

What happens?

It should still run correctly.

So using as is just a nice trick to type less. We like those kinds of tricks.

## Experiment: let's comment out lines

Now type in front of the import lines a pound sign #. Save, and run the script.

What happens?

You should get the same errors as when you deleting the line. Putting a pound sign turns a line of code into a comment. Comment lines are ignored by the computer. It is as if they don't exist. This allows us to write notes to ourselves about what we are trying to do. It also can help when we want to take out a line to see what happens.

Delete the pound sign in front of those two lines. Run the script. It should work again.

### Experiment: read the API notes

The minecraft libraries are also called an API, which stands for Application Programming Interface. In most cases you can think of an API the same as a library. Technically an API is not as much as a library but the description of a library. Let me explain using a burger. When you go to a burger joint, the menu description of a cheeseburger with mayo, lettuce, and tomato tells us what you want to eat. But the description is not the same as the actual burger. 

So the API is essentially the description of how a library should behave, and library that actually makes it behave like that is the actual burger.

The usefulness of this idea, for the young hacker, is that the API notes gives us a quick summary of the words that the library knows. This is handy because getting the code makes it harder to get the list.

I will use the API and the minecraft library interchangabily. 

### Experiment: change a variable name

Find this line:

world.setBlock( x+1, y, z+1, block.STONE)

Now change y for w. Run the code.

What happens?

Yes, you get an error message. 

the letters, x, y, z are variables. A variable is essentially a box where you can put values in it. If the computer doesn't know about the box, it will complain.

The equal sign in Python means assignment. That means, we are putting a value into the variable box. In the line below

[x,y,z] = world.player.getPos()

world.player.getPost() returns a list with values such as [2.23, 4.343, 6.454]. A list is just a line of values that are put in order. Python allows us to assign several variables at once by giving the different position of the list a name.

Assignment most often is done by single variable, and it would look like this:

hello = "Hello world!"

now type that into the code, and copy and paste the following line

print hello

What happens?

In your console, you should see "Hello, world!" running. It won't show up on minecraft. To get it to run on minecraft, type in

world.putIntoChat(hello)

Now run the script and click go back to minecraft. You should see, "Hello, world" there.


### Hacking

* Try changes the values. So instead of 1, change that to two. 
* Look at mcpi/block.py. Find the likst of available blocks. Try changing the value of block.STONE for another existing value.
* Would typing block.ICE_CREAM create an ice cream block? Try it. 
* what if you just put numbers instead of adding and subtracting the x, y z values?
* Come up with something for you to try. What happens? Share it with others.

### Challenge

You should only try the challenge for 5 minutes. Sometimes you will figure it out. Sometimes you won't. But you should try solving it before moving on, and you should stop after 5 minutes.

Try creating a column. This means, instead of putting one block, put two or three blocks on top of each other.

Share if you find anything weird or strange.

# Again, and again, and again

The coordinate system in minecraft.

If you tried the challenge and you know about the coordinate system, you probably ran into a strange thing: they got the coordinates wrong.

So minecraft is essentially one giant block make of little cubes. Those cubes and be air or dirt, but there is a cube in every single spot. The location of that cube is given with three coordinates, x, z, and y.

x and z are the plane. They point how much to the right and left you have moved.y is how high or low you are.

In the U.S. the convention is that x and y are the plane, and z is the hight. But for whatever reason that is not the way it is in minecraft. The reality is that z,y,z is just a convention, and as long as we are away that they are using it differently, it doesn't really matter what names we give it.

#Open colum.py and run it

What happened?

You should have seen a column appear.

Read the code. What is different from the previous code? Can you make sense of wwhat is going on?

When programming we often want to do something over and over again. That is called looping. So rather than typing the same statement again, and again, and again, we use loops.

Python has a few kinds of loops, but let's introduce one of the most useful ones now. It is called the for loop. And it works in the following manner:

for variable_name in list:
  do stuff here

What it does is that it takes a value from the list, and uses that value to execute everything in the for loop block.

In Python, a block of code is marked by white space. hit tab, and everything that lines up is part of the block.

### Experiment: take out the white space

Erase the white space in front of world.setBlock. Run the script. What happens?

You should get an error message.

Let's go back to the code. We find ourselves with this bit 

range(0, height)

What does it do? Let's try it.

### Exploring the python console

Type on the console
python

This will start the python console. Now type 
range(0, height) 

You get an error. We need to assign height. So let's now try
height = 20
range(0, height)

And we get a list. 

So range(0, height) gives us a list that starts at zero and ends at the value of height. Play a bit change the values to see what you get.

You noticed again that the values come within square brackets []. That means that we are using a list. A list, also called an array, is nothing more than a container that holds many values in a certain order. 

Let's go back the code

### Experiment: change range for a list

So let's change range(0, height) for a list

for level in [0,1,2]:

save and run the script. 

What happens?

You should see the script running correctly.

So we know that range(0, height) and [0,1,2] are the same. In this case it would be less typing if we just use the literal array. But what if height was another number instead of three. 

### Experiment: change height for a a bigger value. Much bigger. Yeah, get ridiculous.

Save and run the script.

What happened? 

The blocks would be much higher. Now go back into the console and type range(0, 25). Suddenly using range() makes more sense.

Now let's look at this line:
world.setBlock( x+distance, y + level, z+distance, block.STONE)

You noticed that we are not using the literal numbers anymore. we are using the distance variable. Why? 

Well, it makes things easier for us. Change the distance value. Run the code. You see how easy that was? Now change distance into a literal. Now let's change it again.

As you see, it is faster to use a variable and change the value in one place than having to change it again, and again, and again. Also, if there was an error, we only need to look at a single place.

## Hacking
* Change the height value
* Change the distance value
* Create a new variable to give another distance for the z value
* Take out level what happens?
* Try creating a wall

## Challenges
* How would you get the colum to move?


# Moving 
Now let's move it

# What is it that we need it to do?

#Experiment:
Can you tell me what should happen to make it look like the column moves?

## Writing a to-do list
So we start with a to do list

# erase the column
# move the position of the column
# draw the column
# repeat quickly

This is called pseudo-code. pseudo means "fake." It is not real code because the computer can't understand it. But it let us know what we should learn.

There is a long tradition in computer textbooks that when teaching beginners, we should encourage them to add many comments. 

I am going to buck tradition here: don't. There is a better way. Instead of comments, write functions, and use the comment as the basis for the function name.

So look at the first line of my fake code. It says, "erase." So I am going to create a function that is called, "erase"

In python, you write a function 

def move():
  erase()
  move_position()
  draw_column()

Now let's see. We have a draw_column. We have cod that does that. Let's turn that into a function.

Now we have erase. What does erase do?

It gets the column and turns the blocks into air.

So it is essentially drawing the column into air. We create a function to do that.

So now we have draw and clear. Let's do move position. All what we want it to do is to move a bit to the side. So we update the position to one. Actually, update() sounds like a better name. So let's update.


Let's run it. 

Nothing seems to happen. Let's add a print statement to confirm that it is working.

Hmm, it is running, but we can't see the column moving. Can you figure out what is happening?

So it is happening so fast, that we can't see it. We need to slow down the computer to see what is going on. We need to make the computer go to sleep.

Does the API has a sleep, wait, or do_nothing function command? No.

## How to search for information online

So we know what we want. We want to stop or slow down execution. So open google, and type

python wait

We will get a number of results. Which one should we look at?

In my experience, the third or fourth entry tends to be the best. The first one is often a poor quality site with strong SEO, but the ones belows tend to be high quality links. When searching python, seek the following sites

stackoverflow.com
docs.python.org

or blog entries of professionals. These often have then name of the programmer or end with blogspot.com wordpress.got or github.io

At first it will be hard to see the difference. But over time you will learn what a professional blog looks like. 

The less than good sites tend to have:
Way too many ads
Gimmicky visuals
Pop ups
Pushing you to sign up to see the answer or to download software

You should avoid those.

Let's try another search.

Minecraft PI API

The basic format is

name_of_technology what_I_want_to_find


# Cleaning up with objects
