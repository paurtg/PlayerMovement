# PlayerMovement

Add both of these states to a 3D object with a Player Controller component added to it. One state will allow you to move and control the character around the game scene, including the gravity element with ground checking and a jumping feature.
The other state will allow you to rotate the camera attached to a player, making it able to turn our character around

## Contents

This component is made from the following behaviours:
- `Player Controller`
- `Camera Controller`

And the following states:
- `MouseLook`
- `PlayerMovement`

### MouseLook

When added to the main camera that is attached/following the character or operating as the character's vision, this component manages the camera on the X axis and Y axis. Movement on a Y axis will allow us to move our vision up and down, rotating the camera up and down but with a limitation of 180° so it does not flip behind the character. Movement on a X axis will allow us to turn around from side to side, rotating the body of the character. After being added to the camera, the mouse sentitivity will need to be set and our Player Body will need to be dragged from the Hierarchy to the Inspector.

### PlayerMovement

After removing the collider in our 3D object (player) and adding a Character Controller component to it, we will need to add an empty game object to our character (in the hierarchy) called GroundCheck. In the scene, we will place this right at the botton of the 3D object but still inside its body. This invisible object alongside with code will check what our player is colliding with, detecting what layers are considered Ground and will reset our velocity. Lastly, this component will allow us to jump. When added to our player, we will need to refer the Player Controller and GroundCheck obejcts into the inspector. We will need to create a new layer called Ground and attach it to every object we consider ground, in Ground Mask we will choose Ground. Adjusting the parameters will depend on each type of game. 
