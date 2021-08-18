# Advanced Cards

<sup style="font-size: 90%">(This is a feature unlocked with [***Loot's Tools Plus***](../../plus). A ***Plus*** Account is required.)</sup>

This type of Card lets you execute a Python Script (run.py) when a Card is redeemed.

You can find the "run.py" file on ```<Loot's Tools Folder>/commands/<Card's name Folder>/run.py```

## Install dependencies

Your Python Script might need some dependencies, install them over ```<Loot's Tools Folder>/dependencies/```.

You can do it through pip like this: ```pip install --target="<Loot's Tools Folder>/dependencies/" <packageName>```

## Examples

*Advanced cards*, despite it's name, don't need to be very complex. Let's see some example *Advanced Cards*:

### Shady Search

This *Advanced Card* searches a random query from a list full of weird stuff; enough for creeping out your FBI agent and for your chat to have a good laugh.

#### Code

```python
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

### Do a Barrel Roll! (Windows only)

This *Advanced Card*, clearly inspired by StarFox, makes your screen turn around 360º, doing a Barrel Roll.

#### Code

```python
import rotatescreen

class advCard:
    async def run(self, **args):
        import time
        
        screen = rotatescreen.get_primary_display() # Identificamos la pantalla principal
        start_pos = screen.current_orientation # Pillamos la orientación de la pantalla principal

        for i in range(1, 5): # Lavadora: Giramos 5 veces, aunque la primera vez lo gira a 0
            pos = abs((start_pos - i * 90) % 360)
            screen.rotate_to(pos) # Rotamos a la posición calculada en la anterior linea
            time.sleep(1.5)
```

#### Dependencies

Install the following dependencies in the ```dependencies``` folder:

- [rotatescreen](dependencies/rotatescreen.zip){target=_blank}

### Vodka (Windows only)

This *Advanced Card* changes your keyboard to Russian for 5 seconds and plays Russian-like music to go with the prank.

#### Code

```python
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
