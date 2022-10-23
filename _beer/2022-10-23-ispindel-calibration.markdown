---
layout: post
title:  "iSpindel Calibration"
date:   2022-10-23 8:39:18 -0600
categories: jekyll update
---
[iSpindel](http://ispindel.de) is an IoT based hydrometer for monitoring fermentation. I will likely create a post later on tips for building and source code modifications. The focus here is to capture some wonderful tools that make the calibration process a little easier. The focus of this post is going to be calibration, so let's get started.

Things you'll need
* Large bucket
* Water
* Sugar (2lbs ish)
* Hydrometer or Refractometer
* iSpindel

Before starting make sure the iSpindel's tilt is ~25 degrees in water, if it's greater than 25 you'll need to add some weight to bring it down, and it's connected to a monitoring software or able to be monitored through the wifi config info page.

1. Pick a maximum SG that you'll likely hit. I picked 1.100. 
2. Using the sugar wash calculator [here](https://chasethecraft.com/calculators) calculate how much sugar and water to mix for your maximum SG. Depending on the size of your bucket you'll need to pick a desiered volume, The iSpindel will be mostly floating sideways so the volume doesn't need to be that deep. Minimally make sure it can float at ~80% angle without touching the bottom of the bucket. 
3. Mix the sugar and water based on the above calculation.
4. Put the iSpindel in the sugar water and record the tilt value.
5. Determine what the next SG to measure is. Ususally I just subtract 10 gravity points and continue until it reaches 1.000. You can do less measurments or more depending on your desired accuracy. For me 10 seemed good enough. For example: 1.100 - 10 gravity points is 1.090.  
6. Next you'll want to use dilution calculator [here](https://www.brewersfriend.com/dilution-and-boiloff-gravity-calculator/) to determine how much water to add to dilute the sugar water for the next SG measurment. The calculator takes volume, current gravity, and desiered gravity. If the added water is too much, go ahead and discard some of the original volume in order to not overflow the bucket. I sometimes keep a few small buckets or bowls full of specific gravities so I can double check at the end.
7. Add the amount of water per the calculator and measure the SG with a hydrometer or refractometer. 
8. Repeat steps 5, 6, and 7 until 1.000 is reached.
9. Using this [calculator](https://www.ispindel.de/tools/calibration/calibration.htm) enter all recorded gravity and tilt values.
10. Put the iSpindel into config mode, pushing the reset button twice. Connect to it's wifi and enter the outputted equation into the equation field on the configuration screen. Save the configuration and the iSpindel will restart.
11. After entering the equation into the iSpindel's configuration, I usually put it back into configuraton mode and monitor the info page while putting the iSpindel in some of the saved discarded known gravity buckets. If you're happy with the results, the iSpindel is ready to be connected to your desiered monitoring software, sanatized, and put into fermenting wort.
