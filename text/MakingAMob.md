# Creating a Mob in Minecraft

We are going to create a mob in Minecraft using the Minecraft PI API. This is the API that MOJANG wrote and made available so that people could write mods in the Raspberry PI version of Minecraft. If you don't need a Raspberry PI though; one can use CraftBukkit together with the Raspberry Juice plugin. To make things even nicer, we have created a (craftbukkit distribution)[CraftbukkitDistribution.html] that speeds up installation.

## Breaking down the steps

So let's break down the steps for creating a mob. We should create a body for the mob. We should have the mob being able to move. The mob should be able to see and identify the player. The mob be able to follow the player. And finally, something should happen once the mob touches the player.

So our to do list looks like this:

* [Create a body for a mob](CreateBody.md)
* Give sight to the mob
* Make the mob follow the player
* Create some interaction between the player and the mob

