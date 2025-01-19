# How To Make Dalgona Minigame in Minecraft Bedrock

This is a tutorial on how to make a Dalgona minigame from Squid Game in Minecraft Bedrock.

If you haven't watched [my YouTube video](https://youtu.be/fvBl5o2TpOE), you could watch it first and come back here later to understand

link : [How To Make Dalgona Minigame in Minecraft Bedrock](https://youtu.be/fvBl5o2TpOE)

---

## Commands from my Youtube Video
<img src="images/Commandblock Layout.png" alt="Command Block Layout" width="200" />

### 1st command
>Blocktype  &rarr; Repeat\
>Condition  &rarr; Unconditional\
>Redstone   &rarr; Always Active

```plaintext
/execute as @e[type=thrown_trident] at @s if block ~ ~-1 ~ brown_terracotta run execute as @p[c=1] at @s run playsound block.turtle_egg.crack @a ~ ~ ~ 1 1
```

### 2nd command
>Blocktype  &rarr; Chain\
>Condition  &rarr; Conditional\
>Redstone   &rarr; Always Active

```plaintext
/execute as @e[type=thrown_trident] at @s if block ~ ~-1 ~ brown_terracotta run setblock ~ ~-1 ~ lime_terracotta replace
```

### 3rd command
>Blocktype  &rarr; Repeat\
>Condition  &rarr; Unconditional\
>Redstone   &rarr; Always Active

```plaintext
/execute as @e[type=thrown_trident] at @s if block ~ ~-1 ~ white_terracotta run execute as @p[c=1] at @s run playsound note.bass @a ~ ~ ~ 1 1
```

### 4th command
>Blocktype  &rarr; Chain\
>Condition  &rarr; Conditional\
>Redstone   &rarr; Always Active

```plaintext
/execute as @e[type=thrown_trident] at @s if block ~ ~-1 ~ white_terracotta run setblock ~ ~-1 ~ red_terracotta replace
```

### 5th command
>Blocktype  &rarr; Chain\
>Condition  &rarr; Conditional\
>Redstone   &rarr; Always Active

```plaintext
/execute as @e[type=thrown_trident] at @s if block ~ ~-1 ~ red_terracotta run execute as @p[c=1] at @s run kill @p[c=1]
```

---

## Setup for The Arena

<img src="images/Arena's Setup.png" alt="Arena's Setup" width="200" />

### 1st command
>Blocktype  &rarr; Repeat\
>Condition  &rarr; Unconditional\
>Redstone   &rarr; Always Active

```plaintext
/tp @a[x=-2,y=68,z=-17,dx=10,dy=0,dz=10] 3 70 -6
```

Explanation :<br>
> @a[x=-2,y=68,z=-17,dx=10,dy=0,dz=10]

These x,y, and z arguments correspond to the coordinate of the most-behind corner when you're facing at x and z positive where you don't want the player to be.<br>
The dx,dy, and dz arguments correspond to the dimension of the area relative to the coordinate I mentioned.

<img src="images/1st Command.png" alt="1st Command" width="" />
<br><br>

> 3 70 -6

This coordinate is where you want the player to get teleported to

<img src="images/1st Command(1).png" alt="Command 1st Command(1)" width="" />
<br><br>

### 2nd command
>Blocktype  &rarr; Repeat\
>Condition  &rarr; Unconditional\
>Redstone   &rarr; Always Active

```plaintext
/execute if blocks -2 55 -17 8 55 -7 -2 63 -17 all run say player @p[c=1] has completed this challenge
```

<img src="images/2nd Command.png" alt="Command 2nd Command" width="" />
<br><br>

This command is actively comparing these two layers. If they're identical, this command will send a message to all players indicating a player has completed the game.<br><br>

### 3rd command
>Blocktype  &rarr; Chain\
>Condition  &rarr; Conditional\
>Redstone   &rarr; Always Active

```plaintext
clone -2 59 -17 8 59 -7 -2 63 -17
```
<img src="images/3rd Command.png" alt="Command 2nd Command" width="" />

This command clones the middle layer to the first layer, so after a player completed the game, it'll return to its original form.