# Game Creator Extensions

## Character

### Rotation Units

#### Look at Location

Specify a location for the character to look at.

#### Pawn - Pivot

Has the same behaviour as the Pivot rotation, except that it also can lock its rotation to look at a target. The purpose of this pivot is to avoid a runtime error that happens when changing the facing unit of a character at runtime while inspecting said character.
It is recommended to use this rotation unit when using pawns, especially with the Abilities module.