
## Filter Self

Removes the caster from the potential targets.

## Filter Pawn Only

Targets can be locations, or they can any game object. This will ensure that only [Pawns](../../core/features/pawn.md) are valid targets. 

## Filter Projectile

Filter used in [projectiles](../projectiles/index.md) for abilities that spawns multiple projectiles. This prevent a projectile to collide with another.

## Filter Out of Range

Filter targets that are not in range of the ability at activation time ([#4](../#execution-sequence)).

<figure markdown>
  ![Ability inspector](https://github.com/daimahou/documentation/blob/main/docs/img/filter-range.png?raw=true)
</figure>

- **Leeway**: controls how strictly we are checking ability range. Leeway is added as a percentage to the actual ability range to determine if a target should be hit or not.
- **Max Facing Angle**: defines a cone in front of the caster, targets that are outside of it will be considered out of range. The angle is centered on the character facing direction, e.g. with a value of 180°, the half circle formed by the characters shoulder will be the valid area.

!!! tip "Melee ability avoidance"
    You can set up Melee Abilities using the [Closest Target Targeting System](../targeting/#cast-on-closest-target). 

    With this setup, once the tharget is acquired and the animation initiated, the target will always be hit. However, between the start of the animation, and the resolution of the effects, there might be a time lapse during which the target may move away. 

    This filter will remove any target that moved out of range.