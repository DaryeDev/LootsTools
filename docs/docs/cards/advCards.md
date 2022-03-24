# Advanced Cards

<sup style="font-size: 90%">(This is a feature unlocked with [***Loot's Tools Plus***](../../plus). A ***Plus*** Account is required.)</sup>

This type of Card lets you execute a Python Script (run.py) when a Card is redeemed.

Put the "run.py" file on the Card's folder, that you can open clicking "Open folder" on the Editor's Card's page on the **Loot's Tools' Card Editor**.

---

## Install dependencies

Your Python Script might need some dependencies, install them over ```<Loot's Tools Folder>/dependencies/```.

You can do it through *pip* like this: ```pip install --target="<Loot's Tools Folder>/dependencies/" <packageName>```

---

## Examples

*Advanced Cards*, despite it's name, doesn't need to be very complex.

Let's see some example *Advanced Cards*:

### Shady Search

This *Advanced Card* searches a random query from a list full of weird stuff; enough for creeping out your FBI agent and for your chat to have a good laugh.

[Copy Card "Shady Search" on your Collection with LootsTrading](lootstools://copyCard/5fb23a1bb8df520035382caf){ .md-button .md-button--primary }

#### Code

``` py title="run.py"
import webbrowser
import random
class advCard:
    async def run(self, **args):
        # Weird queries
        turbio = ("panales para adultos", "manzanas de plástico", "cerdos venenosos", "como hacer que me crezca el pelo", "vacunas caseras contra el covid", "casco para el brazo", "descargar ram sin virus", "descargar counter strike 1.6 sin virus", "naranjito", "dacaco046", "bolas", "los mocos producen cancer", "caracoles sin concha", "osos inmaduros" "bicho bola con sombrero", "americano en traje de baño", "boris johnson en traje de baño")
        
        # We get a random query
        item = turbio[random.randint(0, len(turbio))]

        # We URL encode the random query and search it on our default web browser
        import urllib.parse
        webbrowser.get().open(f"https://google.com/search?q={urllib.parse.quote_plus(item)}")
```

#### Dependencies

No extra dependencies.

---

### Do a Barrel Roll! (Windows only)

This *Advanced Card*, clearly inspired by StarFox, makes your screen turn around 360º, doing a Barrel Roll.

[Copy Card "Do a Barrel Roll!" on your Collection with LootsTrading](lootstools://copyCard/60a4050e49450500351a72e2){ .md-button .md-button--primary }

#### Code

``` py title="run.py"
import rotatescreen

class advCard:
    async def run(self, **args):
        import time
        
        screen = rotatescreen.get_primary_display() # It identifies the main display
        start_pos = screen.current_orientation # It gets it's orientation

        for i in range(1, 5): # I feel so clean, like a Washing Machine, oh yeah: It spins 0º, then 90º, then 180º, and then revents to normal.
            pos = abs((start_pos - i * 90) % 360)
            screen.rotate_to(pos)
            time.sleep(1.5)
```

#### Dependencies

Install the following dependencies in the ```dependencies``` folder:

- [rotatescreen](dependencies/rotatescreen.zip){target=_blank}

---

### Vodka (Windows only)

This *Advanced Card* changes your keyboard to Russian for 5 seconds and plays Russian-like music to go with the prank.

[Copy Card "Vodka" on your Collection with LootsTrading](lootstools://copyCard/60a4d9452eae1a0035f2d08d){ .md-button .md-button--primary }

#### Code

``` py title="run.py"
import time
import os
import py_win_keyboard_layout
from playsound import playsound


class advCard:
    async def run(self, **args): 
        previousLayout = py_win_keyboard_layout.get_foreground_window_keyboard_layout() # It grabs the keyboard language to restore it later
        py_win_keyboard_layout.change_foreground_window_keyboard_layout(68748313) # It changes the keyboard layout to Russian
        playsound(os.path.join(args["commandPath"],"kazotsky-kick-3.mp3")) # The song is played
        time.sleep(5) # It waits 5 seconds
        py_win_keyboard_layout.change_foreground_window_keyboard_layout(previousLayout) # It restores the original keyboard language
```

#### Dependencies

Install the following dependencies in the ```dependencies``` folder:

- [py_win_keyboard_layout](dependencies/py_win_keyboard_layout.zip){target=_blank}
- [playsound](dependencies/playsound.zip){target=_blank}

Also, download ```kazotsky-kick-3.mp3``` on the Card's Name folder, on the same one than ```run.py```: [kazotsky-kick-3.mp3](dependencies/kazotsky-kick-3.mp3)

---

## How To

An *Advanced Card*'s Script is written in Python, so I recommend you to have, at least, basic knowledge of it.

It needs to have an special header in order for ***Loot's Tools*** to detect that it's an *Advanced Card*.

``` py title="run.py"
class advCard:
    async def run(self, **args):
```

### Variables

Using an *Advanced Card* also gives us access to information about the redeemed Card, like *[Tags](../cards/normalCards.md#tags)*, but with variables. They are all inside ```args```, and some keys are as follow:

- ```commandPath```: The path of the Card's folder, where ```run.py``` is.
- ```streamer```: The streamer's name.
- ```user```: The name of the user that redeemed the Card.
- ```cardName```: The name of the Card redeemed.
- ```data```: The rest of the redeem data: User Inputs, Rarity, etc
