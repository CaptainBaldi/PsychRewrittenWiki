## Functions

### openCustomSubstate(name:String, ?pauseGame:Bool)
Opens a new substate.

* `name` - The name of the substate to be created.
* `pauseGame` - Whether the game should pause while the substate is active (Default is false).

**Notice:** You can only have one substate active at a time!

### closeCustomSubstate()
Closes the current substate, if there is one.

**Notice:** Calling this function calls `onCustomSubstateDestroy`!!!

### insertToCustomSubstate(tag:String, ?pos:Int)
Inserts a Lua object into the current substate.

* `tag` - The object's string tag.
* `pos` - The position in the substate where you want to insert the object (Default is -1). Anything less than 0 simply "adds" the object to the substate.

***

## Callbacks

### onCustomSubstateCreate(name)
Called when a new substate is created, passing in its name as a parameter.

### onCustomSubstateCreatePost(name)
Called right after `onCustomSubstateCreate`, passing in the same parameters.

### onCustomSubstateUpdate(name, elapsed)
Called every frame while a substate is active, passing in its name and elapsed as parameters (The amount of time in seconds that have passed since the last frame).

### onCustomSubstateUpdatePost(name, elapsed)
Called right after `onCustomSubstateUpdate`, passing in the same parameters.

### onCustomSubstateDestroy(name)
Called when a substate is closed.

***

## Variables

**Notice:** These variables are _hscript exclusive!!!_

* `customSubstate` - Refers to the current substate instance (If no substate is open, this variable will be null).
* `customSubstateName` - Refers to the name of the current substate (If no substate is open, this variable will be "unnamed").

***