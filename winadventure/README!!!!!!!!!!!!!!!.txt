Adventure: Revisited
C++ Version Copyright © 2006 Peter Hirschberg
peter@peterhirschberg.com
http://peterhirschberg.com

Big thanks to Joel D. Park and others for annotating the original Adventure decompiled assembly code.  I relied heavily and deliberately on that commented code!

Original Adventure™ game Copyright © 1980 ATARI, INC.
Any trademarks referenced herein are the property of their respective holders.

Original game written by Warren Robinett. Warren, you rock.

*****************************************************************************************************
::::: Game Controls :::::
*****************************************************************************************************

	1.......................select
	2.......................reset

	SPACEBAR................drop items
	ARROW KEYS..............move player

	ALT/ENTER...............toggle fullscreen mode

The original game had configurable settings that used the left and right "difficulty" switches on the 2600. For Adventure Revisited, please open the adventure.ini file in any text editor to modify the difficulty switch settings.

Press the "select switch" (the 1 key) to choose the game level (I recommend level 1 if you've never played before) and press the "reset switch" (the 2 key) to start that game.

Please refer to the "game instructions.txt" file for detailed instructions on how to play the game.

*****************************************************************************************************
::::: Description :::::
*****************************************************************************************************

Atari Adventure has always been one of my favorite games. Not just for the Atari 2600, but in general. It just has so much heart and personality. I can still, today, play the game and be amazed at the scope and playability of the game. It is truly a classic and a landmark in computer gaming.

So, yeah yeah - I know there are emulators in existence that already run this game perfectly. There are also some recreations out there that add additional levels and such. But emulators require substantial CPU resources to run, which seems pretty wasteful for a game like Adventure and also thereby eliminate many "lo-fi" platforms from running the game (cell phones for instance). None of the simulation/recreations that I have played have the same feel as the original game. They all seem to be completely lacking the "soul" of the original game, and the source code is typically not available and/or platform independent. There is the Atari Flashback version (ewww, what a BAD simulation!). At least the Atari Flashback 2 has a perfect version of Adventure (and a sequel too!) but then of course you have to play the game on your TV.

Finally, I loved the fact that original sources had been decompiled (which provided some pretty cool insights into the game!) and annotated/commented, but I wanted the game to be preserved and documented in a more portable (and readable!) form.

Adventure Revisited is my attempt at creating a lightweight but HIGHLY ACCURATE open-source and platform independent version of the classic Atari game Adventure. I wanted to write something that you could pick up and read to just see how the game worked, or you could take and with very little changes, create a version of the game that could run on a portable device for instance. My original motivation for doing this was so that I could create a version of Adventure that would run on my Treo 600 which incidentally has a resolution of 160x160 - less than that of the original 2600, thus requiring some sub-pixel magic, but certainly doable. The Windows application, minus sound samples, is only 68k. w00t!

So what is Adventure Revisited? Is it an emulator? A simulator. A port? To tell you the truth, I'm not quite sure. This may be the first instance of some sort of bizarre hybrid. As mentioned above, I used a dissassembled and annotated version of the original game's source code as a reference in creating this software. Certain pieces of the code could be considered "emulation" - for example, the player/missile collision detection is, in a way, emulating that particular part of the original hardware. I also kept all the game data in the same format as the original source where practical to ensure the most accuracy possible. I tried VERY hard (obsessively in some cases) to structure my code as much like the original game, simply translating assembly (or the spirit of the original code anyway) into C++ code, so that sort of makes this a port. Other portions of the code I simply “fudged” based on my experience with the game, which would make this a simulator or recreation. The source code is provided, so make your own decision. My estimate would be 5% emulator, 55% port, 40% simulator/recreation. At any rate, you should find it to be very nearly 100% accurate excluding any boo-boos on my part.

And yes - the Easter Egg is exactly as it was in the original. :-)

In closing, I tried pretty hard to keep the core game code platform independent. It should be extremely easy to port this app to other platforms. Simply fill in the provided Platform_XXXX() functions and call the frame function every 1/60 of a second and you're done.

I am providing this code FREE OF CHARGE with the following provisions granted:

   1. The freedom to use and study the work,
   2. The freedom to copy and share the work with others,
   3. The freedom to change the work,
   4. The freedom to distribute changed and therefore derivative works.


And one last time -
Original Adventure™ game Copyright © 1980 ATARI, INC.
Any trademarks referenced herein are the property of their respective holders.








