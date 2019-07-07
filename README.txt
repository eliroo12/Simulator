-------PLEASE NOTE THAT THIS IS A SIMULATION RAN BY A COMPUTER. IT IS ONLY SOMEWHAT REFLECTIVE OF THE CAPABILITIES OF AN AVERAGE PLAYER.------------
------THE MAIN USE AND GOAL FOR THIS SIM IS TO COMPARE STATS, COMPARE OPENERS, AND OVERALL SEE HOW THINGS EFFECT OUR ROTATION.----------
-----DAMAGE VALUES MAY BE 1-2% OFF BECAUSE THE DAMAGE FORMULA ORDERING ISN'T FULLY UNDERSTOOD JUST YET----

Basic Sim functions - Using the GUI:

* You can run at most two different sims at once to compare different stats and openers. If you want to compare you need to just simply make sure that Sim Two has stat information full filled out and the sim will run both
*Opener is where you can choose between defined openers. that are built out in the settings file (More on how to work that later)
* Fights are simply a tool to gauge how downtime effects each job. Currently DNC has delay logic while BRD does not. This feature should never be used to gauge opener and/or stats.
* Length of Fight is how long you want to run the sim in seconds. 
* Run Times is how many times you want to run each sim. More times = More accurate results but will take longer to run.
* Set Party will allow you to pick what part members you have. It requires you to choose at least 7 and will determine what buffs are available.
* If you want to change buff start times click on set buff times and enter in the time manually when buffs are USED (Not when activated).
* Create Logs will create a logfile with your sim results, only recommend for one or two sims as the file will get will large across multiple sims.
* Party Modifier when checked will add in the 5% dex bonus you get from a full party.
* Checking potion will have you use potion at an optimal time on CD. If you put the potion in the opener it will use it there regardless of if this is checked or not.


The settings File:

This file contains the settings, that you can custom add in yourself if you want.

If you want to add in a fight with breaks the formating is as follows:

fight:Fight Name;Delaystart-Delayend-Holdbuffsfordelay(True or False), Nextdelaystart-nextdelayend-Holdbuffsfordelay(True or False)

fight needs to be lowercase


For openers the formating is as follows:

jobopener:Opener Name;Command1,Command2,Command 3, ect.

jobopener can be either dnc or brd depending on what you are designing it for

You can directly input what abilities you want the opener to do and it will do it 100% of the time, it doesn't check conditionals like if X is up if you input it directly this is to make it less rigid and easier to make an opener you want.
There are also special logical commands for openers:

Prepot 1.5  - This will prepot 1.5 seconds before the fight, you can adjust this number if you want to prepot later but 1.5 is about the cast animation on pot.
AutoGCD - Will follow the sims opener GCD logic
AutoOGCD - Will follow the sim opener oGCD logic
AutoPP - Will use Pitch Perfect at 3 Rep
AutoGCDIJ - Will check if you had used Barrage on RA first then use IJ if both dots don't have the same end time(To ensure a post barrage snap)
PreRaging .7 - Will use raging before the fight at X time

TechDrift -  Will force you to drift Technical even at unfavorable GCD Tiers
StandDrift - Will force you to drift Standard even at unfavorable GCD Tiers
ReverseProc - Will either do Reverse Cascade or Fountain depending on proc. This was useful for determining openers but not so useful now

eg Dnc opener:

dncopener:Standard;Prepot 1.5,Standard Finish,Flourish,Technical Step,Devilment,Bloodshower

eg Brd Opener:

brdopener:Prepull;PotionPre 2.2,PreRaging .7,Stormbite,Bloodletter,Minuet,Caustic Bite,Battle Voice,Empyreal Arrow,AutoPP 1,AutoGCD,AutoPP 2,AutoGCD,AutoPP 1,AutoGCD,AutoOGCD 2,AutoGCDIJ,Sidewinder,AutoPP 1,AutoGCDIJ,AutoOGCD 2,AutoGCDIJ


My sim just crashes on load?

You may have messed up the settings files or the images file, try redownloadding the sim


The logic used for each sim will be in joblogic.txt

If you find the Sim doing something offensive or incorrect please feel free to DM on Discord Ellunavi#8710





