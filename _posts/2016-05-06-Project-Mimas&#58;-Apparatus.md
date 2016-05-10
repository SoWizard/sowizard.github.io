---
layout: post
comments: true
---

Finding the perfect platform was a little bit more difficult than I imagined; I'd like to keep this as inexpensive as possible. This post will outline all the gear that I bought along with the respective price and tally it at the end for your convenience and mine.

##  RC Platform

My only requirements for the platform was that it follows Ackermann steering geometry, so that the system models a real car as close as possible. This of course rules out any differential steering platforms that use tracks/treads (tanks etc). Ackermann steering allows the inner wheel to angle itself further into the turn to minimise forces on the wheels and thereby reduce slip. This is necessary because the inner and outer wheel have different radii as they make the turn (thereby different normals to the circle they make). The following Wikipedia figure does an *okay* job of demonstrating the principle. It might be hard to tell but the inner and outer wheel are *not* parallel and thereby make different angles from the turning point origin. Read more about it at this excellent write-up [here](http://www.me.ua.edu/me364/PDF/Steering_Ackerman.pdf).

![Ackermann Steering](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a0/Ackermann_turning.svg/2000px-Ackermann_turning.svg.png)

Different radii on the inner and outer wheel means that in order to keep up with each other, the outer wheel has to spin at a greater speed than the inner wheel. Most RC cars have a front and rear differential which allows the wheels to turn at different speeds. [This](https://youtu.be/K4JhruinbWc?t=1m50s) is a quite excellent old school video demonstrating the need for a differential.

I began my search at HobbyKing. They have a local warehouse in Australia and a substantial range of products. Not only do they sell hobbyist parts but complete platforms as well. Their cars came in at cheaper prices compared the well-known brands like Tamiya but most of the spare parts were on backorder and have been for months (check the comments on the parts). It doesn't take a genius to figure out that this car will run into many walls especially while training to nail down the algorithm, so readily available spare parts are essential.

I ended up purchasing a Tamiya Rising Storm off-road buggy. The Rising Storm has a 1/10 scale, so it's around 40cm in length and 25cm in width. It's based on the DF-02 chassis, which has been on the market since 2004, so cheap parts and mods should be easy to find. It's shaft-driven 4WD from a single brushed electric motor (type 540). Tires are 86mm in diameter and each tire has its own suspension that can be easily adjusted by adding spacers. Stiffening the suspension would allow me to add more load without the chassis touching the ground. The electric motor would preferrably be brushless, but that would require a new motor controller. The buggy runs at a sufficiently high speed and acceleration with this current setup so there's no justifying the cost of upgrading. I'm not even sure I'll be able to get it to autonomously run at its max speed! Eye-balling it, I would say it's maybe around 20-25km/h?

There were cheaper alternatives to the Tamiya at around $120, but I thought the extra investment would pay off in the event that I (or any friends/family) would like to further modify and race this car.

![Tamiya Rising Storm](/images/platform_full.jpg)

### Internals

And here's a shot of it with the top off (oh my, manners!).

![Tamiya Rising Storm internals](/images/platform_top.jpg)

The motor can be seen in the bottom left. You can also see the trapezoidal steering linkage for Ackermann steering. The battery is mounted on the port side and is held down by spring-type split pins. Small tip, you can bend the ends of the split pin so it's easier to hold onto while removing and inserting.

#### ESC and Radio Receiver

These are the only two electronic components need to drive the car.

- TEU-105BK Brushed ESC ([datasheet](https://www.tamiyausa.com/pdf/manuals/45055ml.pdf))
- TRU-08 2.4GHz 2-channel wireless receiver ([transmitter datasheet](http://www.tamiya.com/japan/download/rcmanual/45053.pdf))

![ESC and Radio Receiver](/images/platform_esc.jpg)

ESC stands for Electronic Speed controller. It receives a message from the transmitter as a PWM signal (Pulse Width Modulated, read more here) and 'translates' that into the appropriate power level to the motor. 

The ESC also includes a BEC (as it says so on the front). Don't get me started on the name *BEC*. A BEC is a Battery Elimination Circuit. It *eliminates* the need for another battery to power peripherals like the receiver and servos (and thereby converts the power from the main, large battery into a usable format). The BEC naming convention stems from the RC hobbyist crowd. For all the engineers out there, it's a simple DC-DC converter (I'd say it's a linear regulator but it could be buck or buck/boost). The integrated BEC outputs the voltage at 6.0V. Upon further investigation it's closer to 6.3V. This discrepancy isn't worrisome. 

The input is rated between 6.6V - 7.2V. I'm using a 2S LiPo instead of the recommended NiMH battery, which has a nominal voltage of 7.4V (and higher when fully charged). This isn't much of an issue and can possibly be why the ouput voltage from the BEC is higher than 6.0V.

The single Futuba J (servo cable) from the ESC also powers the TRU-08 receiver. It shares common ground and power with the other ground and power pins on the receiver, which is how the steering servo is powered. 

#### Steering Servo

A servo is attached to the steering linkage to directly control the steering. This is all fairly standard. The servo is of type:

- TSU-03 Servo

I couldn't find a datasheet but after searching online I found the following specs:

`4.8V 44 oz-in. 0.23 sec/60°`
`6.0V 57 oz-in. 0.19 sec/60°`

So it appears it can accept voltages between 4.8V - 6.0V with higher voltages inducing a higher torque. The servo is connected directly to the receiver.

#### Battery & Power

As mentioned before, I opted to choose LiPos instead of NiMH batteries. They seem to be much more common with hobbyists these days and come in all range of sizes and capacities. They also tend to be lighter and have much higher discharge rates (allows for brushless motors to be used). I order a Turnigy 2 cell (7.4V) 3600mAh from HobbyKing. It has a decent 30-40C discharge (side note: at first I was very confused why it's 30-40C. Does it mean the max is 30C or 40C?! Turns out that it means at constant discharge, the max is 30C but it can peak up to 40C for 10 seconds).

The discharge connector was a 4mm bullet connector. XT-60s are again quite polular and a lot of accessories tend to use them. I ordered a few male and female XT-60 connectors from HobbyKing and soldered the female on my batteries. Be sure to use shrink wrap! You dont want exposed wires, especially not on your LiPos.

Unfortunately Tamiya have a proprietary battery connector. Instead of cutting and soldering a new XT-60 connector, I just bought a cheap adapter from HobbyKing.

LiPos are not meant to be discharged completely. It does significant damage to the lifetime of the battery. It turns out that the ESC has an in-built low-voltage cutoff for LiPos but I bought a battery indicator and alarm (also from HobbyKing) to scream out when the battery is running low.

![Battery and adapters](/images/platform_battery.jpg)

[//]: # Insert about second BEC, how to power other electronics, power calculations etc.



## Controllers and Sensors

Coming soon!



## Total

All prices are in AUD. Conversion rate as of late March is around 1 AUD = 0.70 USD.

|      |      |
| :--- | ---- |
|      |      |
|      |      |
|      |      |
|      |      |
|      |      |
|      |      |
| Σ    |      |