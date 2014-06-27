Blade Symphony Game Balance Scripts
============


What you can do with this
============
Check out the repository to your scripts folder located at:
BladeSymphony/berimbau/scripts

You can then make adjustments to the game by changing the contents of these files. For example:

```
Actions
{
  "RyokuFastBase"
  {
    "move_scale"            "1"
    "move_lock"             "0"
    "animation_move"        "1"
    "reaction"              "ACT_BB_STUMBLE"
    "reaction_layer"        "ACT_HIT_UPPER"
  }

  "RyokuReverseString1"
  {
    "factoryclass"          "attack"
    "extends"               "RyokuFastBase"
    "charge_animation"      "ACT_BB_R_C1_CHARGE"         // charge animation activity
    "charge_animation_run"  "ACT_BB_R_C1_CHARGE_RUNNING" // charge animation activity while running

    "tier1"
    {
      "animation"       "ACT_BB_R_C1_T1"                 // attack animation activity
      "move_lock"       "1"                              // can override movement lock; valid values are 0, false, 1, true
      "lock_duration"   "0.28"                           // can override "lock_duration" above
      "damage"          "12"
    }
    "tier2"
    {
      "animation"       "ACT_BB_R_C1_T2"
      "move_lock"       "1"
      "lock_duration"   "0.28"
      "damage"          "16"
    }
    "tier3"
    {
      "animation"       "ACT_BB_R_C1_T3"
      "move_lock"       "1"
      "lock_duration"   "0.56"
      "damage"          "22"
    }
  }

  //  etc...
}
```

Here, RyokuReverseString1 (reverse just means fast stance) inherits all properties from RyokuFastBase, and then on top of that adds its own properties such as damages, lock times, animations, etc

Yes, you can make pull requests! No, we won't be pulling everything you request. However, we will test and make considerations for damage adjustments, lock times, etc. This way you can participate in game balance without sending me Steam messages.

============

This folder and everything within is licensed under Creative Commons Attribution-NonCommercial.
http://creativecommons.org/licenses/by-nc/4.0/