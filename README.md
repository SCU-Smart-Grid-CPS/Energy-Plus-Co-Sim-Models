# Energy Plus UCEF-Compatible House Models

For optimization with a single house in EP and the [EnergyPlusOpt2Fed](https://github.com/SCU-Smart-Grid-CPS/TwoFedEPOpt) or multiple simulations at once using the [Supercontroller](https://github.com/SCU-Smart-Grid-CPS/UCEF-Supercontroller) federation in UCEF.

Tested to work with EP 9-4-0 and UCEF 1.1.0

## FMU Templates

A template is available under "releases" for up to 32 simulations using the [Supercontroller](https://github.com/SCU-Smart-Grid-CPS/UCEF-Supercontroller). Simply place any house model in each folder, and update the config files.


## Sacramento, CA

SAC_hp_UCEF_appliance_v5-5: most up to date model. Validated and used in paper "Economic Benefits of a Novel HVAC Control Strategy in Grid-Interactive Residential Buildings." Stable as of July 2022.

## San Jose, CA

UCEF Template Annual SanJose CA: Compares high and low-income houses. Updated Oct 2022.

## Boise, ID

BoiseID_UCEF_Template_Annual: Compares high and low-income houses. Updated Oct 2022.


## San Francisco, CA

Used in some of our older papers (2021 and earlier).

Models included are the same except for run period:   
EP_UCEF_SF-hp-crawlspace_Jan1-7.idf: Model with dates preset to Jan 1-7   
EP_UCEF_SF-hp-crawlspace_Feb12-18.idf: Model with dates preset to Feb 12-18   
EP_UCEF_SF-hp-crawlspace_Sept27-Oct3.idf: Model with dates preset to Sept 27 to Oct 3    

## Usage Instructions

To run, check the .idf run period and match with the one set in the UCEF federation. 
Change ipconfig.txt in the folder Joe_ep_fmu. Then zip Binaries, ipconfig.txt, and modelDescription.xml and change file extension, saving this as "Joe_ep_fmu.fmu"
Move the .fmu to the same directory as the .idf

Note the included Joe_ep_fmu.fmu will likely not work because the ipconfig is wrong for your computer. 

Recommendation: Keep a clean copy of this folder that is never run, then make a copy with a different name for each new simulation. Otherwise it will overwrite all of the output files and it can be confusing which files belong to which simulation.
