# MakeyMakey-PuzzleMap
Read the clues and find your way through a Makey-Makey connected map

<h3>You Need:</h3>
<ul>
<li>a computer with a browser, a USB port, and speakers</li>
<li>a Makey Makey board</li>
<li>electrical wire (insulated)</li>
<li>alligator clips (I used 8)</li>
<li>decorative (but conductive) wire, such as beading wire</li>
<li>a stretched canvas</li>
<li>paint (I used acrylic)</li>
</ul>

<h3>Step One - Puzzle Design</h3>
<ol>
<li>design symbols</li>
<li>pick a six symbol answer</li>
<li>design map (be careful to avoid getting too close to the edges of the map)</li>
<li>paint/print puzzle</li>
</ol>

<h3>Step Two - The Wiring</h3>
<ol>
<li>Use beading wire to recreate the symbols on the map, poking the wires through to the other side of the canvas.
(some of my designs fell over the wooden frame of the canvas and were more difficult to poke through, so please take that into consideration)
I broke the symbols down into small straight segments and added them in like staples.
You will have to add wire to both the correct and red herring symbols, otherwise the answer would be pretty obvious.</li>
<li>Flip over the canvas and use the insulated electrical wire to attach all of the symbols that are not part of your final solution together.
Make sure to strip the wire so the metal of the wire is touching the metal of the beading wire.
Note: while you could normally solder the wires together, solder and acrylic paint can probably release unhealthy fumes, and canvas can catch fire, so I used tape.</li>
<li>Use an alligator clip to attach the dummy symbols to the space bar part of the Makey-Makey board.
<li>Add six male to male wire connectors to the W A S D F G ports on the back of the Makey-Makey board. 
<li>Use alligator clips to attach the back of each remaining symbol to the other end of its respective wire connector to the Makey-Makey board. The first key to W, the second to A, and so on.</li>
<li>Use a last alligator clip and attach it to a ground on the Makey-Makey board and a conductive object that the user will hold while solving the puzzle.</li>
<li>Plug in the Makey-Makey board to the computer via USB</li>
</ol>

<h3>Step Three - The Browser (webpage)</h3>
<ol>
<li>In between the head tags of the document use the audio tag to preload any sound you want to play when the puzzle is solved
<li>Write a JavaScript script that listens for “key downs” from the keyboard, stores the entries and checks them against an expected password.
In my code the end goal is "W,A,S,D,F,G" and every time a new key is pressed on the map, the value is pushed onto the end of the 6 value password array and the oldest entry is shifted off. The function that pushes and shifts the array does not accept the same key twice in a row to allow for the player accidentally pressing the same key multiple times.
If the password is correct the browser plays the selected sound.
(please see index.html for more detailed comments on how the JavaScript works)</li>
</ol>

<h3>Step Four – Solve the Puzzle</h3>
<ol>
<li>Load the html page onto a browser</li>
<li>While holding the ground to the Makey-Makey board in one hand, use the other hand to solve the puzzle.</li>
</ol>
