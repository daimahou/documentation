!!! warning "Targets & effects"
An important thing to understand is that each effect applies once per target, *e.g. if you set up the Targeting System to capture multiple targets and set an Effect to spawn one projectile, you will effectively spawn one projectile per target*.

## Debug log

Prints a log message in the console. The message will be prefixed with the target name or location. Useful to understand what targets have been captured by the system.

<figure markdown>
  ![Ability inspector](https://github.com/daimahou/documentation/blob/main/docs/img/effect-debug.png?raw=true)
</figure>

- **Message** : the message to print.

## Instructions

Execute a generic Game Creator [instruction list](https://docs.gamecreator.io/gamecreator/visual-scripting/actions/). Note that the arguments for the instructions are as follow :

- **Self** : the caster
- **Target** : the current ability target

<figure markdown>
  ![Ability inspector](https://github.com/daimahou/documentation/blob/main/docs/img/effect-instruction.png?raw=true)
</figure>

- **Description** : replace the title in the inspector. Useful for organization.

## Sound effect

Play a sound effect.

<figure markdown>
  ![Ability inspector](https://github.com/daimahou/documentation/blob/main/docs/img/effect-sfx.png?raw=true)
</figure>

- **Max Occurences** : limits the number of time this sound effect will be trigger by this ability
- **Audio Clip** : the clip being played
- **Audio Config** : see Game Creator [audio configuration](https://docs.gamecreator.io/gamecreator/visual-scripting/actions/instructions/audio/play-sound-effect/) for more info.

## Projectile

Spawns one or more projectile(s). See the [projectile documentation](../projectiles/index.md) for more details.

- **Projectile** : the projectile to be spawned.
- **Spawn Method** : the way projectiles are spawned.
- **Spawn Point** : the origin of the projectile

### Spawn methods

#### Single Spawn

Spawn a single projectile.

<figure markdown>
  ![Ability inspector](https://github.com/daimahou/documentation/blob/main/docs/img/effect-projectile.png?raw=true)
</figure>

- **Direction** : direction the projectile is spawned in.
- **Destination** : planned destination of the projectile.

#### Arc Spawn

Spawn projectiles distributed around a cone shape.

<figure markdown>
  ![Ability inspector](https://github.com/daimahou/documentation/blob/main/docs/img/projectile-arc.png?raw=true)
</figure>

- **Spawn Count** : number of projectiles to be spawned.
- **Radius** : radius of the cone shape, controls how far the projectiles are spawned from the spawn point.
- **Arc Angle** : angle of the cone shape. Controls the width of the spawn.
- **Spawn Delay** : spawn rate in seconds. If 0, all the projectiles will be spawned at a time.
- **Max spawn duration** : will reduce the spawn delay to allow all the projectiles to be spawned within the duration.
- **Random Spawn** : Will randomize the position of each projectile within the cone.

#### Circle Spawn

Spawn projectiles distributed around a circle.

<figure markdown>
  ![Ability inspector](https://github.com/daimahou/documentation/blob/main/docs/img/projectile-circle.png?raw=true)
</figure>

- **Spawn Count** : number of projectiles to be spawned.
- **Radius** : radius of the cone shape, controls how far the projectiles are spawned from the spawn point.

## Impact

Spawns an impact at the target location. See the [impact documentation](../projectiles/index.md) for more details.

<figure markdown>
  ![Ability inspector](https://github.com/daimahou/documentation/blob/main/docs/img/effect-impact.png?raw=true)
</figure>

- **Impact** : the impact to be spawned.


## Composite effects

Composite effects are special effect containers that add additional functionality to the previous effects. Composite effects can be combined with one another to create an arbitrarily complex setup.

### Delayed effects

Add a delay to the effects.

<figure markdown>
  ![Ability inspector](https://github.com/daimahou/documentation/blob/main/docs/img/effect-delay.png?raw=true)
</figure>


- **Description**: string field used to customize the title in the inspector. Useful to keep organized.
- **Delay**: delay after which the effects are applied.

### Conditional effects

Add [requirements](../requirements) to the effects to be applied. If the requirements are not met, the effect will simply be skipped.

<figure markdown>
  ![Ability inspector](https://github.com/daimahou/documentation/blob/main/docs/img/effect-cond.png?raw=true)
</figure>

!!! tip "Burn with Fire !"
You can easily use these conditional effects to add additional damage on a fireball if the enemy is affected by the status effect "Burn". Using the [module Stats](https://docs.gamecreator.io/stats/) will help a long way to create this kind of effect.