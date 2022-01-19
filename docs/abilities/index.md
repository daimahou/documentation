# Welcome to Abilities

Every RPG lovers have dreamt of their ideal ability systems, thought about how spells would interact with each other to create interesting dynamics. Creating such systems is a difficult task, this is why we developed Abilities, *a series of tools that will allow you, the designer, to implement YOUR ideas intuitively in a short amount of time*.


---

# General information

## Who is it for ?

Abilities has been created for **designers**. The philosophy behind abilities is to create a wide set of tools that designers can use to craft their own abilities without the need for additional code. Built upon [Game Creator 2](https://gamecreator.io/), you get access to an incredible wealth of tools to supercharge your creativity.

Abilities is packed with features of its own, targeting system, animation synchronization, projectiles and more. Designed to play well with other modules, you can **stop worrying about technicalities and focus on making games**.

## What is it ?

A suite of tools that allows the designer to create abilities with synchronized animation and effects.

- **[Reactive Gesture](../core/features/gestures.md)**: allows you to synchronize animation effortlessly

- **[Abilities](ability-asset/index.md)**: allows you to create abilities with customizable components.

- **[Projectiles & Impacts](projectiles/index.md)**: allows you to configure projectiles with custom trajectory, spawn pattern and impact effects.


Abilities are defined by 5 different sub-systems designed to be flexible and easy to use.


- **[Targeting system](ability-asset/#targeting-system)**: Let you choose how the targets are selected.

- **[Activation system](ability-asset/#activation-system)**: Let you choose how the ability is executed - e.g. is it a direct spell or a chanelled spell.

- **[Requirement system](ability-asset/#requirement-system)**: Let you define conditions that needs to be met for the ability to can be casted - e.g. cooldown, mana cost, or even arbitrary conditions.

- **[Filter system](ability-asset/#filter-system)**: Let you define conditions that needs to be met for a target to be valid. Useful for removing friendly fire, or to create conditional effects - e.g. targets need to be on fire to be affected.

- **[Effect system](ability-asset/#effect-system)**: Let you specify what the ability will do once valid targets have been selected - e.g. applying damage, spawning projectiles, etc.


## How does it work ?

Very simple, yet extremely powerful approach. There is only 4 steps to create all the abilities you dreamt of.


1. Configure your animations using the reactive gesture system to synchronize your effects and instructions precisely how YOU want.

1. Configure your ability strategies so they apply to the targets of YOUR choice.

1. Specify the effects of your ability to match YOUR design.

1. Spice up your ability by adding projectiles and impact which you can customize to create the abilities YOU envision.


## Errata

If you find a mistake or omission in the documentation, please send us an email at [daimahou.studio@gmail.com](mailto:daimahou.studio@gmail.com) with a link to the relevant entry and an explanation what you think is wrong. We'll take a look and make any necessary updates.