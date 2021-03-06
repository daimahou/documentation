# Activation System

## Single

The single activation starts an animation and waits for it to finish, ending the ability. Effects will be applied after receiving an activation notification from the animation.


<figure markdown>
  ![Ability inspector](https://github.com/daimahou/documentation/blob/main/docs/img/Activation.png?raw=true)
</figure>

- **Animation** : [Reactive Gesture](../../core/systems/gestures.md) containing the animation to play.

- **Face Target** : When enabled, turn the character to face the target. Rotation speed is defined by the [Motion Unit](https://docs.gamecreator.io/gamecreator/characters/component/#motion).

- **Walk in Range** : When enabled, this will cause the character to first walk within [range](../#ability-inspector) of the ability

!!! Danger "Runtime Error"
    When **Face Target** is enabled during the execution of an ability, if the character is selected in the inspector, there will be an error. This is due to how Unity & Game Creator handle serialization and this will only happen in the editor. To avoid this, we recommend that you use our custom [Rotation Unit](https://docs.gamecreator.io/gamecreator/characters/component/#rotation) **Look at Target - Pivot**.
    <figure markdown>
      ![Ability inspector](https://github.com/daimahou/documentation/blob/main/docs/img/rotation%20unit.png?raw=true)
    </figure>
    This unit is a hybrid between **Pivot** and **Look at Target**, it acts as a Pivot when no targets are available, and acts as Look at Target when no targets are available.
    The need for this custom Rotation Unit is only to avoid the runtime error in the editor.

## Channeling

The channeling activation starts a looping animation and executes its effects a fixed number of times every second while the key is pressed down.

- **Face Target** : When enabled, turn the character to face the target. Rotation speed is defined by the [Motion Unit](https://docs.gamecreator.io/gamecreator/characters/component/#motion).

- **Gesture State** : [Reactive Gesture State](../../../core/systems/gestures/#reactive-gesture-state) containing the animation to play.

<figure markdown>
  ![Channeling Activator inspector](../../../img/channeling.png)
</figure>

## Charging

Coming soon