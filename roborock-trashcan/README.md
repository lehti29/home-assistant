
# Roborock trashcan

Assumes you have the Xiamio home integration installed.

How to use these blueprints:
1. Create a counter
    1. In HA GUI, go to Configuration -> Helpers
    2. Press "Add Helper"
    3. Choose Counter
    4. Choose a nice name
    5. Set minimum value to 0, and Maximum value to N -1, where N equals after how many cleanings you want to send the vacuum to your trashcan. Set Ininitial value to the same as maximum value
    6. Choose Stepsize to 1
    7. Create
2. Go to Configuration -> Blueprints.
3. Add The url for each blueprint:
    1. https://github.com/lehti29/home-assistant/blob/main/roborock-trashcan/decrement-counter.yaml
    2. https://github.com/lehti29/home-assistant/blob/main/roborock-trashcan/goto-trashcan.yaml
    3. https://github.com/lehti29/home-assistant/blob/main/roborock-trashcan/reset-counter.yaml
4. For each, press "Create automation", select corresponding inputs (the counter and the vacuum for all three)
    1. To be able to send the vacuum to the location for your trashcan, you need the coordinates (to input in goto-trashcan.yaml). You can retrieve those via the Flolevac app. Download that. This is what I did:
    2. Enter the credentials you use for Xiomi Home
    3. In the hamburger menu, go to "map"
    4. In the bottom left corner, press "GO"
    5. On the map, press where you would like the vacuum to go, and a pin will be dropped there.
    6. Long press "Go there". The coordinates will be copied to your clipboard like so: [xcoord, ycoord]
    7. These are the coordinates that should be inputted in "goto-trashcan.yaml"
5. Have fun!
