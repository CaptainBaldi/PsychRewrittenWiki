## Basic Functions

### makeLuaSprite(tag:String, ?image:String, ?x:Float, ?y:Float)
Creates a static Lua sprite.

* `tag` - The string tag you want to assign the sprite to.
* `image` - The image you want the sprite to display when drawn.
* `x` - The initial X position of the sprite (Default is 0).
* `y` - The initial Y position of the sprite (Default is 0).

### makeGraphic(obj:String, width:Int, height:Int, color:String)
Generates a simple rectangular graphic for a sprite.

* `obj` - The sprite's string tag.
* `width` - The width of the graphic to be generated (Default is 256).
* `height` - The height of the graphic to be generated (Default is 256).
* `color` - The color of the graphic to be generated (Default is "FFFFFF" or "white").

### addLuaSprite(tag:String, front:Bool)
Adds a Lua sprite to the game.

* `tag` - The sprite's string tag.
* `front` - Whether the sprite should be added in front or behind character groups (Default is false).

### removeLuaSprite(tag:String, destroy:Bool)
Removes a Lua sprite from the game.

* `tag` - The sprite's string tag.
* `destroy` - Whether the sprite should be permanently destroyed (Default is true).

**Notice:** If you fully destroy a sprite, you will have to recreate it using `makeLuaSprite` before you can add it again!

***

## Animation

### makeAnimatedLuaSprite(tag:String, ?image:String, ?x:Float, ?y:Float, ?spriteType:String)
Creates a Lua sprite that can easily have animations assigned and played.

* `tag` - The string tag you want to assign the sprite to.
* `image` - The image you want the sprite to display when drawn.
* `x` - The initial X position of the sprite (Default is 0).
* `y` - The initial Y position of the sprite (Default is 0).
* `spriteType` - The type of the sprite's animation (Default is "sparrow"). A full list of available sprite types can be found [here](https://github.com/ShadowMario/FNF-PsychEngine/blob/experimental/source/psychlua/LuaUtils.hx#L250).

### addAnimation(obj:String, name:String, frames:Array(Int), framerate:Int, loop:Bool)
Adds an animation a sprite via individual frames.

* `obj` - The sprite's string tag.
* `name` - What the animation should be called.
* `frames` - An array containing the frames the animation should have.
* `framerate` - The frames per second the animation should play at (Default is 24).
* `loop` - Whether this animation should loop (Default is true).

### addAnimationByPrefix(obj:String, name:String, prefix:String, framerate:Int, loop:Bool)
Adds an animation to a sprite via prefixes.

* `obj` - The sprite's string tag.
* `name` - What the animation should be called.
* `prefix` - The animation prefix on your atlas or other data source.
* `framerate` - The frames per second the animation should play at (Default is 24).
* `loop` - Whether this animation should loop (Default is true).

### addAnimationByIndices(obj:String, name:String, prefix:String, indices:String, framerate:Int, loop:Bool)
Adds an animation to a sprite via animation indices.

* `obj` - The sprite's string tag.
* `name` - What the animation should be called.
* `prefix` - The animation prefix on your atlas or other data source.
* `indices` - A list of frame indices. This can either be a string, with frames being separated by a comma (e.g., '1, 3, 5'), or an array (e.g., {1, 3, 5}).
* `framerate` - The frames per second the animation should play at (Default is 24).
* `loop` - Whether this animation should loop (Default is false).

### playAnim(obj:String, name:String, forced:Bool, ?reverse:Bool, ?startFrame:Int)
Plays a sprite animation.

* `obj` - The sprite's string tag.
* `name` - The name of the animation.
* `forced` - Whether the animation should restart if the sprite's current animation is the one being played (Default is false).
* `reverse` - Whether the animation should play backwards (Default is false).
* `startFrame` - What frame the animation should start on when played (Default is 0).

### addOffset(obj:String, anim:String, x:Float, y:Float)
Adds the specified X and Y offset to an animation on a sprite.

* `obj` - The sprite's string tag.
* `anim` - The name of the animation.
* `x` - The amount of X offset to add to the animation.
* `y` - The amount of Y offset to add to the animation.

***