# Controller

A controller is an asset that represents a player controller in game. It is used to easily bind controls to functionality.

A controller holds a series of input mappings which can be interpreted by each respective modules to create gameplay behaviour. Each button can be simply bound to a regular unity input action to customize which button corresponds to which action.

For a concrete example, have a look at the [Abilities input module](../../../abilities/input.md).

<figure markdown>
  ![Controller example](https://github.com/daimahou/documentation/blob/main/docs/img/input_abiliy.png?raw=true){ width="600" }
  <figcaption>Controller example</figcaption>
</figure>


## Creating a new controller

Controllers are scriptable objects and to create one, you'll need to right click on the Project Panel and navigate to Create → Game Creator → Input → Controller.
