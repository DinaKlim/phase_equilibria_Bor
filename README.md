# phase_equilibria_Bor
TLDR: James Connolly's Perplex page https://www.perplex.ethz.ch/ and the examples https://www.perplex.ethz.ch/perplex_examples.html is all you need for calculating phase diagrams

My favorite thermodynamics course page is here https://www.perplex.ethz.ch/thermo_course/ - very useful for understanding what happens behind the Perplex' scenes 

# The fun part of my PhD

I like phase diagrams, so I wanted to take the composition of the massive sulfide from Bor and see if I can reproduce the observed mineral assemblages from the deep, high temperature porphyry part to shallow, low temperature part. 
As an additional step, I wanted to see whether I can model the aqueous fluid that is co-existing with those sulfides; I was interested to see what aqueous S species would be prevalent in this fluid. 

The first step is to take the composition of the ore and calculate a phase diagram at a certain temperature; to do that with Perplex, one should indicate the pressure, too. I tried to come up with reasonable assumptions based on the depth of the ore formation, but after calculating 152 phase diagrams during the revision process, I saw that no matter what pressure you put into the calculation file, the boundaries on the phase diagram do not change. Temperature, however, influences these boundaries a lot. 

## Step 0: download Perplex programs and data files
https://www.perplex.ethz.ch/

Add the modified solution model and thermodynamic database files from this repository

[thermodynamic database](https://github.com/DinaKlim/phase_equilibria_Bor/blob/main/elsup.dat)

[solution model](https://github.com/DinaKlim/phase_equilibria_Bor/blob/main/solution_model_elsup.dat)


## Step 1: chose your composition, your thermodynamic data file and your solution model file
Run build.exe (one of the program files downloaded during step 0) and answer all the prompts to create your own problem definition file

Or take the example file that corresponds to one of the compositions of ore samples from Bor (Serbia) 
[composition of a sample with covellite-pyrite epithermal vein](https://github.com/DinaKlim/phase_equilibria_Bor/blob/main/1_195.dat)

## Step 2:
Run vertex.exe to calculate the phase diagram

## Step 3: 
Run pssect.exe for visualization

## Step 4:
Run werami.exe if you are interested in overlaying the fluid composition contours on top of your sulfide equilibrium assemblage diagram, and Matlab scripts https://www.perplex.ethz.ch/perplex/ibm_and_mac_archives/Perple_X_MatLab_scripts.zip for plotting the contours of the fluid compositions

## Step 5: 
Overlap the fluid composition contours onto your phase diagram. The original lines may be a little "stepped" because the calculation is done on a grid, but after some cosmetic changes the diagram looks like this 

![sulfide assemblages and fluid composition](https://github.com/DinaKlim/phase_equilibria_Bor/blob/main/sulfides_and_fluid.jpg)

Stable ore mineral assemblages (black) at fixed T in the presence of H-O-S fluid; green and blue dashed lines delineate the 50/50 predominance fields for the fluid species at high pressure of 100 bar and low pressure of 0.2 bar respectively, red dashed lines indicate the sulfur condensation curve. Abbreviations: bn = bornite, ccp = chalcopyrite, cc = chalcocite, cpr = cuprite, cv = covellite, hem = hematite, mag = magnetite, po = pyrrhotite, py = pyrite, tn = tenorite

## Optional Step
If your phase diagrams faced last-minute criticism from some members of your committee, and if you received numerous revisions to make after your defense, this song might be good for your mental health
[Zombies ate my pirate ship](https://www.youtube.com/watch?v=8SyaFPfDLCc&list=RDMM8SyaFPfDLCc&index=1)
