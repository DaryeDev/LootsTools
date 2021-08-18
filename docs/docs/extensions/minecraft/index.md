# LootsToolsEX for Minecraft

<sup style="font-size: 90%">(This is a feature unlocked with [***Loot's Tools Plus***](../../plus). A ***Plus*** Account is required.)</sup>

![TwitchEX](img/MinecraftEX.png){: style="height: 150px;width: 150px;float: left;margin: 20px;"}

*LootsToolsEX for Minecraft* is an *EXtension* which allows the interactivity between **Minecraft** and ***Loot's Tools***.

It makes possible sending **commands** to the game and **giving pets** to players in the game.

You can see some example clips of *LootsToolsEX for Minecraft* in-game [here](https://www.youtube.com/watch?v=BqhNUN1Ft6w){target=_blank}, [here](https://www.youtube.com/watch?v=LNAmppbpLXA){target=_blank}, or [here](https://www.youtube.com/watch?v=LBEQGj77ftQ){target=_blank}.

---

## Setup

It's needed for this *EXtension* to work a *Paper*, *Bukkit* or *Spigot* Minecraft server, and this plugin ([LootsToolsSpigot.jar](LootsToolsSpigot.jar)) installed on it.

It's **very important** to start **first** Loot's Tools and **then** the Minecraft Server.

---

## Commands

(Note: the name between parenthesis is the function's name, used for calling them with [Advanced Cards](../../cards/advCards.md)' Scripts)

### MINECRAFTCMD (minecraftCMD)

This command sends a command to Minecraft to execute.

#### Usage

```MINECRAFTCMD {command}```

#### Arguments

- **command** [str]: The command you want to execute on Minecraft.

### MINECRAFTPET (minecraftPet)

This command summons a Pet for the player specified on Minecraft.

#### Usage

```MINECRAFTPET {petAttributes}```

#### Arguments

- **petAttributes** [json]: The pet's atributes. Example: ```{"Type":"DOG","Owner":"ALL","Name":"woof"```.

##### Pet Attributes

- ```Type```: The type of Pet. Possible values: ```DOG```, ```CAT```, ```PARROT```.
- ```Owner```: The Owner of the Pet. If it's ```ALL```, a Pet is given to every player online.
- ```Name```: The name of the Pet.

---

## Additional Notes

If on the commands of [```MINECRAFTCMD```](#minecraftcmd-minecraftcmd) you put ```%PLAYER%```, that command is done for every player online, replacing the tag for their names.
