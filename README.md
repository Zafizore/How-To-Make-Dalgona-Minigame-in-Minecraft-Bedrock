# How To Make Dalgona Minigame in Minecraft Bedrock

This is a tutorial on how to make a Dalgona minigame from Squid Game in Minecraft Bedrock.

If you haven't watched [my YouTube video](https://youtu.be/fvBl5o2TpOE), you could watch it first and come back here later to understand

link : [How To Make Dalgona Minigame in Minecraft Bedrock](https://youtu.be/fvBl5o2TpOE)

---

### Code from my Youtube Video
<img src="images/Commandblock Layout.png" alt="Local Image" width="200" />

#### 1st command
>Blocktype  &rarr; Repeat\
>Condition  &rarr; Unconditional\
>Redstone   &rarr; Always Active

```plaintext
/execute as @e[type=thrown_trident] at @s if block ~ ~-1 ~ brown_terracotta run execute as @p[c=1] at @s run playsound block.turtle_egg.crack @a ~ ~ ~ 1 1
```

#### 2nd command
>Blocktype  &rarr; Chain\
>Condition  &rarr; Conditional\
>Redstone   &rarr; Always Active

```plaintext
/execute as @e[type=thrown_trident] at @s if block ~ ~-1 ~ brown_terracotta run setblock ~ ~-1 ~ lime_terracotta replace
```

#### 3rd command
>Blocktype  &rarr; Repeat\
>Condition  &rarr; Unconditional\
>Redstone   &rarr; Always Active

```plaintext
/execute as @e[type=thrown_trident] at @s if block ~ ~-1 ~ white_terracotta run execute as @p[c=1] at @s run playsound note.bass @a ~ ~ ~ 1 1
```

#### 4th command
>Blocktype  &rarr; Chain\
>Condition  &rarr; Conditional\
>Redstone   &rarr; Always Active

```plaintext
/execute as @e[type=thrown_trident] at @s if block ~ ~-1 ~ white_terracotta run setblock ~ ~-1 ~ red_terracotta replace
```

#### 5th command
>Blocktype  &rarr; Chain\
>Condition  &rarr; Conditional\
>Redstone   &rarr; Always Active

```plaintext
/execute as @e[type=thrown_trident] at @s if block ~ ~-1 ~ red_terracotta run execute as @p[c=1] at @s run kill @p[c=1]
```

