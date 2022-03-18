# Ability

The most fundamental part of Abilities is the Ability asset. It represents an action a character can perform in-game and comes packed with a collection of flexible and independent features that can be used to customize and control the way abilities work and feel in your game.

## Creating an ability

Abilities are scriptable objects and to create one, you'll need to right click on the Project Panel and navigate to Create → Game Creator → Abilities → Ability.

<figure markdown>
  ![Ability creation](https://github.com/daimahou/documentation/blob/main/docs/img/new%20asset%20menu.png?raw=true){ width="600" }
  <figcaption>Creating an ability</figcaption>
</figure>

## Ability Inspector

An Ability asset will appear, with a list of sections that can be expanded or collapsed so it is easy for the user to modify and organize their abilities.

<figure markdown>
  ![Ability inspector](https://github.com/daimahou/documentation/blob/main/docs/img/inspector_1.png?raw=true){ width="600" }
  <figcaption>Ability inspector - folded</figcaption>
</figure>

The **ID** value is a unique text that represents an ability. When creating a new asset, it will be completely unique. However, duplicating an existing ability will also duplicate the ID and a red message will appear above stating that there are two items with the same ID.

To solve that, expand the field and click on the Regenerate button to create a new unique ID. You can also type in a name if you follow a naming convention that ensures that all item IDs are unique.

The **Icon field** is used to represent the ability in UI, if not set, a white square will be used instead.

The **Range field** represents the distance within which the ability can reach.

## Main features

An Ability is defined by a scriptable object inside your project folder. It is organized into multiple collapse-able sections, each of which controls a very specific feature of this system.

- **Targeting** : An input system that allows you to change how the targets are acquired by the system. Automatically find the closest target, centers around the caster or at the mouse click are some of the different options.

- **Activation** : Controls how the ability activates its effect on the target and how input is processed. Some options are a single activation driven by an animation, or a channeling effect that stays active as long as it is on.

- **Requirements** : Define conditions which need to be met in order for an ability to be cast-able. Some requirements can also prevent an ability from activate and/or apply a cost to it, *e.g. cooldown or mana cost.*

- **Filters** : Define conditions that are used to filter the valid targets for your ability, *e.g. filtering the caster to prevent friendly fire.*

- **Effects** : Controls what the ability actually do, once it has activated and found valid targets, *e.g. damaging a target, spawning projectiles or explosion impacts and more.*

<figure markdown>
  ![Ability inspector](https://github.com/daimahou/documentation/blob/main/docs/img/inspector_2.png?raw=true){ width="600" }
  <figcaption>Ability inspector - unfolded</figcaption>
</figure>

## Execution sequence

1. When the ability is triggered, the **Requirement system** determines if the ability can be executed.

1. The **Targeting system** triggers the input and determines the location the ability will activate from.

1. The **Requirement system** determines if the ability can be activated and activation costs are paid.

1. The **Activation system** decides how the ability will play out. Typically an animation is played using the Reactive Gesture system. Then, the animation sends a signal back to complete the activation.

1. The **Targeting system** works together with the Filter system to determine the valid target(s).

1. Finally, the **Effect system** applies the effects on the valid targets.

<figure markdown>
  ![Ability inspector](https://github.com/daimahou/documentation/blob/main/docs/img/execution-order.png?raw=true)
</figure>

!!! Note "Context Menu"
You can access a context menu by right clicking on most elements.
Elements can be replaced or disabled and documentation can be accessed through it.

## Systems

### Targeting System

The targeting system is responsible for handling player *input* and *acquiring targets*.

A *target* can be any game object or location.

Depending on the system used, targeting happens in two phases. Once before activation to find the target location, and once after the activation to confirm the targets (c.f. [#2 & #5 in the above graph](#execution-sequence)).

Some settings have automatic input, *e.g. Cast on Self will automatically use the caster as a target*, while others will require the player input, *e.g. Cast on Location requires the player to click on the ground*.

<figure markdown>
  ![Ability inspector](https://github.com/daimahou/documentation/blob/main/docs/img/Targeting-2.png?raw=true)
  <figcaption>Targeting systems</figcaption>
</figure>

!!! note "AI Input"
A target can be submitted directly to the ability using an instruction to allow AI to use abilities as well. Refer to the Instructions section for more information.

### Activation System

The activation system is the centerpiece and dictates how the ability works.

The most basic activation type is the [Single activation](activation/#single), the ability starts with an animation, applies its effects once, and then completes its execution with the end of the animation.

Other activation types are Channeled and Charged activation.

At the moment only the [Single activation](activation/#single) type is implemented, but more will be added in future updates.

### Requirement System

The requirement system is responsible for controlling when the ability is use-able as well as managing its success conditions. Additionally it is also responsible for effects that are considered costs, *e.g. cooldowns and mana costs*.

<figure markdown>
  ![Ability inspector](https://github.com/daimahou/documentation/blob/main/docs/img/requirements.png?raw=true)
</figure>

The requirements defined by this system are of 2 types :

- Requirement for use [(#1)](#execution-sequence): Condition that needs to be met in order to cast the ability. In case of failure the ability will simply not start.
- Requirement for Activation [(#4)](#execution-sequence): Condition that needs to be met in order for the effects to resolve. In case of failure, the animation will stop and the ability will fail.

Additionally, a requirement can sometimes have a *side-effect* (which is applied during the activation [(#4)](#execution-sequence)), e.g. entering cooldown, or paying mana cost.


### Filter System

The filter system is responsible for filtering targets according to filtering conditions. The most basic one is to filter out the caster to make sure the ability cannot backfire.

<figure markdown>
  ![Ability inspector](https://github.com/daimahou/documentation/blob/main/docs/img/filters.png?raw=true)
</figure>

### Effect System

The effect system defines what the ability will eventually do to its targets. This system is further enhanced by the [projectiles & impacts](../projectiles/index.md) system.

<figure markdown>
  ![Ability inspector](https://github.com/daimahou/documentation/blob/main/docs/img/effects.png?raw=true)
</figure>