# beagle-servo

Very simple servo controller for Beaglebone Black. Under development.

v0.0.1


## Installation
```
npm install "git://github.com/teisnet/beagle-servo.git"
```

## Usage
```js
var s = require("beagle-servo");

var servo1 = new s.servo('servo1');
var servo2 = new s.servo('servo2', 'P9_22');

servo1.setAngle(-90);
servo2.setAngle(45);

console.log("Servo 1 angle = " + servo1.angle);
console.log("Servo 2 angle = " + servo2.angle);
```

## Notes
beagle-servo is dependent on Bonescript but this dependency is omitted from package.json. The npm build process for the bonescript library is cumbersome and requires the python-compiler opkg package. As Bonescript is already available on Beaglebone as a pre-installed global npm package, no local module and cumbersome build process is necessary.
