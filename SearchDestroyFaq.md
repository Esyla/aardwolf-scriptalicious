# Search and Destroy (including Triple Pack) #

Common questions and problems with Search and Destroy Triple Pack.  If you do not find your question here.. write a note to me.

```
board personal
note write winklewinkle
```

# Questions #
**I get two listings for the same mob.  When i kill one of them, the other one disappears: (for example)**
```
a treant             - labyrinth*
a treant             - 'The Labyrinth' (14965) - citadel
```

_This is because aardwolf lists Campaign targets without telling us if it's a room or area campaign.  As a result it's close to impossible to accurately detect if it's referring to the **area** The Labyrinth or the **room** The Labyrinth... so i am forced to list both._

**When I get a demon school student as area campaign target, I get two every time, one listed in soh and one in sohtwo. Killing just one (in soh) gives credit for both.**
```
a demon school student - soh
a demon school student - sohtwo
```

_This is because the area is listed as "School of Horror" which is the name of 2 areas! It could be the area "soh" or "soh2". So I list both areas for the one mobbecause there is no way to tell which one it means._

**There are a couple 'xrt {area}' that run through bad spots. How can i tell mapper to avoid these rooms?**

_Depending on the version of Mushclient you have you can either 1) Put a level lock on the exit that leads to that aggro room, or 2) make a Custon Exit (aka cexit) that runs you around the problem area. Also using "xset mark" to mark the area's "first" room can sometimes help with routing problems_