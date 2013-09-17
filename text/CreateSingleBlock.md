# Create a single block

Creating a single block is the closest thing to the "Hello, World" script in the Minecraft API. copy and paste the code below into a file, or use the source code provided in the distribution package. 

      # Creating a block
      import mcpi.minecraft as minecraft
      import mcpi.block as block

      world = minecraft.Minecraft.create()

      # Get the player's current position and store the coordinates
      [x,y,z] = world.player.getPos()

      world.setBlock( x+1, y, z+1, block.STONE)

Go back to Minecraft. You should see a single block appear next to you.

Using the API is simple. to communicate with the server, we use minecraft.Minecraft.create(). This object give us access to the world that the player is in. Then we get the position of the player, and we set the block next to us to stone.

And interesting feature here is the realization that everything in minecraft is a block. What appears to be open space is actually air blocks. So technically we are not create a block but transforming it. Yet because it is useful to think as us creating blocks, I will keep using that term.

At this point [creating a column](CreateAColumn.html) is trivial. 
