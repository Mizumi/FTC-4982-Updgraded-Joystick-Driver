FTC #4982 Updgraded Joystick Driver
==================================

FIRST Tech Challenge Team #4982's Upgraded Joystick Driver for use with RobotC.  This driver simplifies usage of joysticks even further, with automatic value updating and on-the-fly swapping of joysticks via software.

No more calling those pesky joystick update functions - just access the values directly and they're guaranteed to be up-to-date:

```
#include "upgradedJoystick.h"

task main()
{
  int y = upJoystick.joy1_y1;
  
  //Do stuff.
}

```

Do you need to swap controllers during a match, but your operators don't have time to physically exchange them?  No problem; software joystick switching is built into the upgraded joystick driver:

```
#include "upgradedJoystick.h"

task main()
{
  //Flip joysticks.
  if (upJoy1Btn(9)) flipJoystick(true);
  
  //Unflip joysticks.
  else if (upJoy1Btn(10)) flipJoystick(false);
  
  //Do stuff.
}
```

If you have any questions, don't hesitate; send them to brandon@mechakana.com!
