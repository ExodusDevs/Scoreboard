# ScoreboardLib
A framework to create easy and fast scoreboards in PocketMine-MP

## How to use the Scoreboard API?

First declare the file as:

```php

use exodus\scoreboard\Scoreboard

```

Then create the instance with the 'Player Class' and 'Title', in this case ``Test Scoreboard``

```php

// must have class: pocketmine\player\Player

$scoreboard = Scoreboard::create($player, "Test Scoreboard");

```

Now spawn the scoreboard to add your line

```php

$scoreboard->spawn();

```

How do I add a line to the scoreboard? simple as this

```php

$scoreboard->setLine(0, "https://github.com/ExodusDevs");

```

You want to delete the scoreboard, do the following

```php

$scoreboard->remove();

```

Or do you want to delete a specific line? here is the code to remove it

```php

//You must go the number of the line you want to delete if you will not delete an incorrect line

$scoreboard->removeLine(0);

```

Or do you go for the easiest to, remove all lines? do this from once man

```php

$scoreboard->removeAllLine();

```

Or better you don't want to delete anything but add all the lines you want just once? I recommend this

```php

//remember this is in beta, I haven't tested it and I think it has bugs anyway open a pull request

$scoreboard->setAllLine([
  "linea 1",
  "linea 2",
  "linea 3", 
  "wallenetwork.xyz"
]);

```