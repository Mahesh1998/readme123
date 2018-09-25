# Introduction

The required task is to command the drone to fly at an altitude to provide rescue to the needy. This is achieved in two ways: first using manual control and then under autonomous control.

# Requirements:

<ol>
<li>Components are assembled to build the CrazyFlie 2.0 quadcopter by following <a href="https://www.bitcraze.io/getting-started-with-the-crazyflie-2-0/">these steps</a>.</li>
<li>CrazyRadio PA USB dongle is used to establish communication between CrazyFlie and PC.</li>
<li><a href="http://zadig.akeo.ie/">Zadig</a> (libusbK) driver for dongle installation. </li>
<li><a href="http://www.headsoft.com.au/download/pc/VJoySetup.exe">Vjoy</a> software is used as virtual controller to provide keyboard control.</li>
</ol>

## The manual control can be done in two ways:

<ol>
<li>Using a Mobile application.</li>
<li>Using keyboard control via <a href="https://github.com/bitcraze/crazyflie-clients-python/releases">CrazyFlie CF client</a>.</li>
</ol>
Autonomous control of a quadcopter can be handled by any of the scripts written in python/C++.Appropriate callbacks are created, which check against transition criteria dependent on the current state. If the transition criteria are met, it will transition to the next state and pass along any required commands to the drone.

# Drone API:

cflib is an API written in Python that is used to communicate with the Crazyflie and Crazyflie 2.0 quadcopters. It is intended to be used by client software to communicate with and control a Crazyflie quadcopter.

The library is asynchronous and based on callbacks for events. The library doesn't contain any threads or locks that will keep the application running, it's up to the application that is using the library to do this.
## Python code structure:
<ol>
<li>URI:<br>
<ul><li>All communication links are identified using an URI (Uniform Resource Identifier).</li> <li>Radio connection is established to provide interface with quadcopter.</li></ul></li>
<li>Python structure:<br>
<ul><li>Functions used from cflib library are fetched from MotionCommander class and can be directly applied to perform the required operations.</li> <li>SyncCrazyFlie is used as a connection protocol.</li></ul></li>
</ol>

## Steps to finally execute the code and make the crazyflie fly:
<ol>
<li>Turn on the crazyflie and place it on the ground.</li>
<li>Plug in the CrazyRadio in the computer.</li>
<li>Activate the python environment and run the script.</li>
</ol>
