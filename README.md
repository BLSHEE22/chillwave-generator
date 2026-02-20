# Chillwave Generator
An engine that randomly generates chillwave music.

## Setup

1. Download Logisim-evolution at https://github.com/kevinawalsh/logisim-evolution.
<br>

2. Open `randomMusic.circ`.
<br>

3. If program memory (ROM 4k x 8) is not already populated...
- Right-click on the tile.
- Click 'Load Memory Image' and import `randomMusicMipsCode.txt`.
<br>

4. If the 'kahdeg MIDI' folder is not already in the top left-hand menu...
- Go to 'Project->Load Library' and select 'JAR Library'.
- Open the 'midi-env' folder, select 'midi-env.jar', and open it.
- You should now see a 'kahdeg MIDI' folder in the top left-hand menu.
<br>

5. Now go to 'Simluate' and make sure the 'Auto-Tick Frequency' is set to 500 Hz.
<br>

6. Reset the simulation (command-R for Mac).
<br>

7. At the very bottom of the circuit, you should see a 'Sustain Pedal' module. 
- Flip switch '2' to lock the sustain pedal in place.
- Make sure there is 0 signal sending through the 'Pedal' tunnel. This means the damper is off!
- How it should look with the sustain pedal locked:
  - !['N/A'](locked_sustain.png)
<br>

8. Start the simulation clock (command-K for Mac).
- You should see the circuit begin to execute. It will now wait for your input parameters that will decide the tonal center, scale, and melody type of the generated music.
<br>

9. Click the input box which says 'HERE' next to it using the 'Hand' tool.
<br>

10. Enter an integer which represents the **tonal center** and press Enter.
- Options:
  -  0 = A
  -  1 = A#/Bb
  -  2 = B
  -  3 = C
  -  4 = C#/Db
  -  5 = D
  -  6 = D#/Eb
  -  7 = E
  -  8 = F
  -  9 = F#/Gb
  - 10 = G
  - 11 = G#/Ab
  - 12 = High A
  - 13 = High A#/Bb
  - 14 = High B
  - 15 = High C
<br>

11. Enter an integer to represent the **scale type** and press Enter.
- Options:
  - 0 = Major
  - 1 = Minor
  - 2 = Dominant
  - 3 = Chromatic
<br>

12. Finally, enter an integer to represent the **melody type** and press Enter.
- Options:
  - 0 = Normal
  - 1 = Angry
  - 2 = Thoughtful
  - 3 = Confused
<br>

13. Now type -1 into the input box and press Enter. 
- This tells the script to start making music based on the suggestions you gave!
<br>

14. If there are no MIDI blocks attached to the circuit (bottom right)...
- You will need to add these in yourself. 
- They can be found in the 'kahdeg MIDI' folder.
- How it should look with MIDI block present:
  - !['N/A'](midi_block.png)
<br>

### IMPORTANT NOTE 
Once you drop of one these bad boys in, you'll most likely be operating blind for the next three.
 
When dragging in a MIDI block blindly, I try to line up my cursor with the middle of the 5 wires and between 2-3 units to the right of the connection point. It might take a couple of tries, but I promise it'll be worth it!

Once you've got all four MIDI blocks in there, sit back, unwind, and enjoy the chillwave.
