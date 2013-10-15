beagle-servo
============

Simple servo controller for Beaglebone Black


Installation
============
npm install "git://github.com/teisnet/beagle-servo.git"


Usage
============
var s = require("beagle-servo");

var servo1 = new s.servo('servo1');
var servo2 = new s.servo('servo2', 'P9_22');

servo1.setAngle(-90);
servo2.setAngle(90);

console.log("Servo 1 angle = " + servo1.angle);
console.log("Servo 2 angle = " + servo2.angle);


Notes
============
beagle-servo is dependent on bonescript, but the npm build process for this library is cumbersome and requires the python-compiler opkg package. As bonescript is already installed as a global package on Beaglebone, the dependency is omitted from package.json, to avoid the build process. 
