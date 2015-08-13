# SpriteLightKit

SpriteLightKit brings back the old two buffered blend trick to get pseudo lighting with just sprites. It handles the setup process of getting that second buffer blended with your normal scene.


![how it works](http://cl.ly/c7Xq/687474703a2f2f636c2e6c792f6336784c2f7370726974656c696768746b69742e706e67.png)

The same scene with two different ambient light setups:

![low ambient light](http://cl.ly/c7Lf/darker.png)
![brighter ambient light](http://cl.ly/c7DN/lighter.png)


## Setup

- create an empty GameObject as a child of your main camera and add the SpriteLightKit component
- add the SpriteLightKitImageEffect component to your main camera and drag the SpriteLightKitBlendImageEffect.shader into the inspector in the shader property
- set the Light Layer in the SpriteLightKit component, which is the layer you want to place your sprite lights on
- remove the Light Layer from your main camera's culling mask so that it does not render the sprite lights
- create some sprites using the SpriteLightMaterial and make sure they are on the Light Layer you chose in the previous step


You can set the ambient lighting by changing the background color of the camera on the SpriteLightKit GameObject. Each of your lights can use the normal sprite tint color to change how it affects the underlying scene.


Lights look best when they are white and falloff to 0 alpha. That lets you use the tint color to color the lights. Setting the tint color's alpha lets you set the intensity of the lights. Get creative with your light shapes and experiment! If you need to occlude lights (if you have walls where light shouldn't pass for example) you can just use any black sprite and place it so that it blocks the light however you want it to.


### Credit

The sweet little town sketch is from the amazing work of @pixelatedcrown. Follow on Twitter and [Tumblr](http://pixelatedcrown.tumblr.com/) to see more awesome art!



#### License

[Attribution-NonCommercial-ShareAlike 3.0 Unported](http://creativecommons.org/licenses/by-nc-sa/3.0/legalcode) with [simple explanation](http://creativecommons.org/licenses/by-nc-sa/3.0/deed.en_US) with the attribution clause waived. You are free to use SpriteLightKit in any and all games that you make. You cannot sell SpriteLightKit directly or as part of a larger game asset.
