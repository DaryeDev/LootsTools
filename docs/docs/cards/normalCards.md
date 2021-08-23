# Cards

This type of Card reads the commands in the file "run.txt" to interpret and, then, execute them.

You can find the "run.txt" file on ```<Loot's Tools Folder>/commands/<Card's name Folder>/run.txt```

---

## Examples

Normal cards are pretty easy to make, let's see a couple of examples:

### Alt+F4

This infamous prank, on a Card form, would be as simple as IRL: only pressing two keys and watch the rage emerge.

( If you have **[LootsTrading]("../additionalFeatures/lootsTrading")** enabled, you can copy the card by clicking here, without writing anything or downloading nothing: [[Alt+F4](lootstools://copyCard/5fb7e18069cff0003945a512)] )

This is as easy as one command:

    SEND alt+f4

The ````SEND```` command sends a combination of keys, being the best for easy mischiefs like this or Rickrolls... >:)

### Gift Chest

Having a "*You won a Chest*" Card in any streamer's Streamloots Collection is very common, and a strike of luck always gets a smile on the spectator's face, but it always interrupts the action on the stream; here's the Solution: (Also as easy as one command ;D)

( If you have **[LootsTrading]("../additionalFeatures/lootsTrading")** enabled, you can copy the card by clicking here, without writing anything or downloading nothing: [[Gift Chest](lootstools://copyCard/5e692668982ade003456a0c2)] )

    CHEST {user} 1

Not only can we adjust the number of chests given to the user by changing 1 to the desired quantity, but also the Collection, by adding it by the end: ````CHEST {user} 1 Tazos Darye!````, being ````Tazos Darye!```` the name of the Collection you want to gift a Chest of. If none is determined, the default Collection will be selected.

Lastly, we see ````{user}````, Loot's Tools will replace this kind of Tag with the respective info, in this case, the user that redeemed the card. More information later on Tags.

### Goodbye Stream!

Chat always likes to troll a bit, and nothing is worse than literally letting them close the stream your people are watching.

This can be achieved by *EXtensions*, a feature of [***Loot's Tools Plus***](../../plus), and in this case, we will be using the OBS one, which allows control over this streaming tool on things like ending stream, changing source settings, changing texts...

( If you have **[LootsTrading]("../additionalFeatures/lootsTrading")** enabled, you can copy the card by clicking here, without writing anything or downloading nothing: [[Goodbye Stream!](lootstools://copyCard/5fa9381dc1826900346e680c)] )

To cut off the stream with a Card, this is the command it has to execute:

    OBSSTREAMING stop

(You can always use as many Commands as you want, obviously, but I focused the examples on fun little commands that will refresh your streams.)

---

## Commands

By default, ***Loot's Tools*** offers a selection of Commands:

### CHEST

This Command allows the Streamer to gift a certain amount of Packs of a given collection to a user.

#### Usage

````CHEST {user} {quantity} {collectionName}````

#### Arguments

- **user** [str]: The user to gift the Pack to.
- **quantity** [int]: The amount of Packs to gift.
- **collectionName** [str] (Optional): The Collection you want the Pack to be of. If not given, it defaults to the main Collection.

### WRITE

This Command simulates being the keyboard and writes the given string.

#### Usage

````WRITE {text}````

#### Arguments

- **text** [str]: The string to be written.

### RUN
This Command runs a program.

#### Usage

````RUN {path}````

#### Arguments

- **path** [str]: The path to the program to run.

### SEND

This Command simulates being the keyboard and sends a key combination.

#### Usage

````RUN {keyCombination}````

#### Arguments

- **keyCombination** [str]: The key combination to send.

### WAIT

This Command waits x seconds to resume execution of the Card's Commands.

#### Usage

````WAIT {seconds}````

#### Arguments

- **seconds** [int]: The number of seconds to wait.

### RND

This Command chooses a random item from a list and saves it to a *Tag*.

#### Usage

````RND({tagName}) {itemList}````

#### Arguments

- **tagName** [str]: The Tag name to save the value into.
- **itemList** [list]: The list of items to choose from, they have to be separated by ", " (A colon and a space). Example: ````item1, item2, item3````

### PRINT

This Command prints on the ***Loot's Tools*** Console Log.

#### Usage

````PRINT {text}````

#### Arguments

- **text** [str]: The text to print.

---

## Tags

*Tags* are a way to introduce variables on Commands when making them, let's see what *Tags* are available:

### {user}

This *Tag* is substituted by the user that redeemed the Card, useful for gifting Packs or making personalized rewards.

### {streamer}

This *Tag* is substituted by the Streamer that the user is redeeming the Card on.

### {cardName}

This *Tag* is substituted by the name of the Card redeemed.

### {rarity}

This *Tag* is substituted by the name of the rarity of Card redeemed.

(Possible values: ````common````, ````rare````, ````epic```` or ````legendary````)

### Additional Tags

If the Card requires input, the input's internal name can be used as a *Tag*.

For example: ![Card's Input](img/AdditionalTags.png)

In this Card, an additional *Tag* would be ````{message}````.

---

## EXtensions

*EXtensions* are a feature unlocked with [***Loot's Tools Plus***](../../plus) which allow for Normal Cards to have even more Commands available.

The *EXtensions* currently available are the following:

- [Loot's Tools EX for Minecraft](../../extensions/minecraft)
- [Loot's Tools EX for Twitch](../../extensions/twitch)
- [Loot's Tools EX for OBS](../../extensions/obs)

Learn more about EXtensions [here](../../extensions) and about each EXtension on their respective page.