#Help on getting the most out of Fiendish's mapper plugin

# Disclaimer! #

Hi, I didn't write it, but I use it and leverage it in my plugin.  **Fiendish's mapper plugin**. To use my triple pack you're going to want to know these fundamentals first!

# Creating CExits (aka Custom Exits) #
## To open a door ##
```
   mapper cexit open n;;n
```
This will **teach** to mapper to open a door and walk through it.

### Detailed Steps ###
  * find a closed door north
  * type **mapper cexit open n;;n** (note the 2 ;'s)
  * wait 2 seconds, you will see a blue mapping confirm message..

### To Test ###
  * go south back to the first room
  * close the door north
  * on the clickable map.. click on the room north of you
  * you will see the mapper open the door and walk you through it

## To get into tricky/annoying areas ##
Some areas require CExits to get into them.. and excellent example is "First Ascent".  To see First Acent's speedwalk with cexit type **speedwalk first**
```
Area Name                       Speedwalk 
The First Ascent                run 19s4w;climb the chain
```

Type **speedwalk** for a full list of areas with cexits.

### Detailed Steps ###
  * Go to the Aylor room `GreyAsh Alley to Silvermist Road` (from Recall type **run 19s4w**)
  * type **exits**  to see the command for the custom exit (in this case it's **climb the chain**)
  * type **mapper cexit climb the chain**
  * wait 2 seconds for mapper to confirm the room

### To test ###
  * recall
  * type **xrt first**

# To Add a Portal to your Mapper #
  * Have an alias that gets the portal out of your bag, holds it, enters it, puts the portal back in your bag, and re-holds whatever you were holding. (_in this example we will use one called "portal\_losttime"_)
  * Invoke that alias and stand in the room where the portal takes you
  * Note the **listed** level of the portal (do not take tier into account)
  * Type **mapper portal portal\_losttime** (for example), when prompted, type in the portal level
  * Done!  Now Mapper will take your portals and level into consideration when calculating the fastest path!

## Making a basic portal alias ##

**You will NEED to change "bag", "hold/dual" and "myOldItem" for this to work!**

```
<aliases>
  <alias
   match="port *"
   enabled="y"
   expand_variables="y"
   ignore_case="y"
   sequence="100"
  >
  <send>get '%1' bag
hold '%1'
enter
hold/dual myOldItem
put '%1' bag</send>
  </alias>
</aliases>
```

### Usage ###
The following would work for mapping an envelope of xyl portal
  1. go to the portal destination
> 2) type
```
mapper portal port envelope
```