The village will have the following resources:
* Fruits
* Meat
* Stone
* Gold
* Wood

*Each resource can be obtained in various ways, such as hunting, mining, farming, or simply attacking and stealing resources from other villages.

The player can build the following buildings:
*House: Required to generate villagers (you can generate up to 3 villagers for each house you own).
Materials required to build a house: 19 wood, 12 stone, 1 gold.
Building requirement: 20 (the sum of the construction attribute of the population must be at least 20).

*Coliseum: Required to generate soldiers (you can generate up to 2 soldiers for each coliseum you own).
Materials required to build a coliseum: 30 wood, 25 stone, 6 gold.
Building requirement: 40 (the sum of the construction attribute of the population must be at least 40).

*Stable: Required to generate riders (you can generate up to one rider for each stable you own).
Materials required to build a stable: 50 wood, 40 stone, 10 gold.
Building requirement: 60 (the sum of the construction attribute of the population must be at least 60).

Village population types:
* Builder: Ideal for construction.
* Warrior: Ideal for attacks.
* Soldier: An improved version of the warrior (you need a coliseum to generate a soldier).
* Rider: An improved version of the soldier (you need a stable to generate a rider).
* Miner: Ideal for mining.
* Villager: Very versatile, good for most resource-gathering activities, though weak in attack and construction.
* Hunter: An improved version of the villager for hunting.
* Farmer: An improved version of the villager for farming.
* Lumberjack: An improved version of the villager for chopping wood.

The village interface will feature an activity record (buffer) showing the user the actions they add before executing them.
The interface includes 7 action buttons:
*Hunt: Asks how many members to send hunting to obtain meat.
*Farm: Asks how many members to send farming to obtain fruits.
*Mine: Asks how many members to send mining to obtain gold and stone.
*Chop: Asks how many members to send chopping wood to obtain wood.
*Flirt: Asks which member to reproduce. Restrictions:

Builder:
  - Only one can be generated at a time.
  - Requires 10 fruits, 2 meat, 1 gold.

Warrior:
 - You can generate up to 2.
 - Requires 3 fruits, 7 meat, 2 gold.

Soldier:
 - Requires a coliseum.
 - The maximum number that can be generated depends on the number of coliseums.
 - Requires 5 fruits, 10 meat, 3 gold.

Rider:
 - Requires a stable.
 - The maximum number that can be generated depends on the number of stables.
 - Requires 10 fruits, 16 meat, 4 gold.

Miner:
 - Only one can be generated at a time.
 - Requires 7 fruits, 5 meat.

Villager:
 - Requires a house to generate them.
 - The maximum number of villagers depends on the number of houses.
 - Requires 3 fruits, 1 meat.

Hunter:
 - Only one can be generated at a time.
 - Requires 10 fruits, 1 gold.

Farmer:
 - Only one can be generated at a time.
 - Requires 5 meat, 1 gold.

Lumberjack:
 - Only one can be generated at a time.
 - Requires 5 fruits, 5 meat, 1 gold.

*Build: Asks what to build; house, coliseum, or stable. The code will check if there are enough materials to build.
	If there are, an image of the building will appear in the village, and the user can place it wherever they want as long as it's a valid location.
	Once the location is chosen using the arrow keys, pressing enter will place the building, and it can no longer be edited.
	Only one type of building can be constructed at a time (to build another, click "play"), and no other action can be performed while constructing.

*Attack: First asks how many members of the village you want to send to attack; the program will simulate a rival and then show your power level and that of the rival.
	With this information, you can decide to either proceed with the attack or surrender. The implemented algorithm allows decisions based on priorities.

For example, if we have 3 villagers and 3 miners and select the "mine" option with 3 people, the algorithm will choose to send the 3 miners for the task, not the villagers.
Similarly, in an attack, all the strongest troops will always be sent first to achieve maximum power.
	Overall, the algorithm is able to identify priorities when performing tasks in the village.

* The player will always have a text area that informs them of what is happening in the village, as well as buttons for each action on the screen, which, when pressed, will add actions to the buffer to be executed once the "execute" button is pressed.

* Likewise, the player or village will always be on alert for rivals; an algorithm generates random rivals at an undetermined time, who will constantly want to attack. In this case, there are two options: Defend or Surrender. Each action has its consequences. If you surrender, you won’t lose troops, but you will lose resources based on your rival's power. Conversely, if you defend, you won’t lose resources, but you will lose a portion of your population proportional to the rival's level.
