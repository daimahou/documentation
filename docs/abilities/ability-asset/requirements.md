## Cooldown

This requirement adds a cooldown to the ability. When a cast is requested ([#1](../#execution-sequence)), the ability will fail if it is currently on cooldown. In case of success, the ability will enter its cooldown period at the activation time ([#4](../#execution-sequence)). 

<figure markdown>
  ![Ability inspector](https://github.com/daimahou/documentation/blob/main/docs/img/req-cooldown.png?raw=true)
</figure>

- **Cooldown**: cooldown duration in seconds.

!!! check "Stats Synergy"
    Owning the [Stats module](https://docs.gamecreator.io/stats/) ? More power to you ! You can set the cooldown to use a [formula](https://docs.gamecreator.io/stats/formulas/) and with a little set up, you can have abilities that have smaller cooldown as they level up !


## In Range

This requirement will cancel the ability if the target is out of range at activation time ([#4](../#execution-sequence)). 


## Custom

This requirement allows you use any Game Creator conditions with the requirement system.

<figure markdown>
  ![Ability inspector](https://github.com/daimahou/documentation/blob/main/docs/img/req-custom.png?raw=true)
</figure>

- **Description**: string field used to customize the title in the inspector. Useful to keep organized.
- **Method**: defines the type of requirement.
    - *Use* : conditions to starting the ability
    - *Activation* : conditions to apply the effects.