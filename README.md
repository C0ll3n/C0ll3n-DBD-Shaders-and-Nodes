# C0ll3n-DBD-Nodes

## Content
### Dedicated Shader

*It's a dedicated shader with a toggle to choose between Legacy-style or IDGAD-style hair; the inputs change depending on the selection.*

- C0ll3n DBD Hair

<img width="288" height="163" alt="v2 3 5" src="https://github.com/user-attachments/assets/df5d08d5-3e6f-4f01-8650-409ec7d9566c" />

<img width="303" height="788" alt="v2 3 5SS2" src="https://github.com/user-attachments/assets/cdb49a17-9fea-40be-8ad8-7c7d30c1b204" /><img width="303" height="606" alt="v2 3 5SS3" src="https://github.com/user-attachments/assets/7d2625d7-3ed4-4510-b330-795d3a9518be" />

### Hair Composite Nodes

*These are nodes that attempt to convert certain parameters from the dedicated shaders to the Bubba or Lance Quen shaders*

- C0ll3n Hair composite
- C0ll3n HC Simple [IDGAD]

<img width="626" height="446" alt="v2 3 5SS10" src="https://github.com/user-attachments/assets/5d175c61-408d-44f2-bca9-e2bdd38d43c1" />

### Custom Hairs (Swapping/Remapping)

*The IDGAD Hairs node group must be connected to one of the shaders that accept IDGAD texture inputs; it can be used with any shader that processes these textures. Hair Styles is a standalone shader that offers more features because it uses more textures than IDGAD can provide on its own, even with the Flow map*
*Requires to remap the UV's using a Hair Guide texture (Included in the blend file) in UV Editor*

- C0ll3n IDGAD Hairs
- C0ll3n Hair Styles

<img width="527" height="434" alt="v2 3 Info4" src="https://github.com/user-attachments/assets/497d693c-1ee1-4d67-9741-af7ba5fc09f2" />

### Parallax/Offset

*These are groups of nodes designed to create the effect of adding more hair, which is useful for models with very little hair. The effect varies depending on the viewing angle, but it requires support from a shader; it can be either IDGAD or Legacy*
*You need to create 3 more copies of the original texture, depending on which one you're working on (IDGAD or Legacy), no apply for Simple version*

- C0ll3n Parallax/Offset [Inputs]
- C0ll3n Parallax/Offset [Outputs]
- C0ll3n Simple Parallax

<img width="915" height="225" alt="v2 3 5SS11" src="https://github.com/user-attachments/assets/60b63c19-ca6f-4903-8bb5-6116f93338df" />

### Extra Node Groups

*These are groups of nodes that function as additional add-ons: “Sun Damage” adds a gradient to “DBD Face Sun Damage” within Bubba's nodes, leaving a visible mark along the edges; “Texture Color Influence” is only for editing colors, saturations, etc., of a color texture (BC); “Custom Tip/Root Color” is only useful on hair whose UVs' have been changed—such as Legacy wigs—to use IDGAD shaders or the dedicated Hair Styles shader, and "DBD JD IDGAD" is a node group made by JD that only work for Bubba shaders that expect those inputs (Specular, Roughness, and Scatter)*

- Sun Damage Gradient
- Texture Color Influence
- Custom Tip/Root Color
- DBD JD IDGAD

<img width="782" height="329" alt="v2 3 Info5" src="https://github.com/user-attachments/assets/20ddca96-6133-41c4-94ca-af36cf00f9fc" />

### Hair Guides

*These are alpha textures for use it as a guide designed for wwork with custom hairs node and/or shader and remap UV's of your hair model, this process can be done in UV Editing in Blender; for being append, you have to go in 'Image' folder; HairGuide_IRS it's a texture for IRS texture made by Bubba, but it needs to be imported maually (IRS.png inside 'Image' folder) using a 'Texture Image' node and connect it in any IDGAD shader*

- HairGuide_Curly
- HairGuide_Dreadlocks
- HairGuide_IRS
- HairGuide_Straight
- HairGuide_Unkempt

<img width="132" height="242" alt="v2 3 SS3" src="https://github.com/user-attachments/assets/744508a9-e7c3-4845-9a03-2fb18e32b5e9" /> <img width="167" height="99" alt="v2 3 SS4" src="https://github.com/user-attachments/assets/eeddfb1c-14b3-4e14-aeb3-a08387706cae" />

*Within 'NodeTree' you'll find more nodes with parentheses '(Don't Import)' and more textures in 'Image'. You can completely ignore these, as each one is imported internally into the same Shaders or Node Group being used*

## Usage Examples

### Dedicated Shader

- C0ll3n DBD Hair (IDGAD)
<img width="835" height="654" alt="image" src="https://github.com/user-attachments/assets/f4d7afaf-5981-44f8-abc0-d51ace4293bd" />

*In this shader, you can connect textures directly. Everything else is handled by the shader itself without needing to add anything extra, unless you want to experiment. However, what I consider necessary for customization is already built in.*

*If you want to modify the brightness, simply adjust the 'Roughness' and 'Specular Shared' parameters.*

*The Root Color and Tip Color transitions, and their blending, are handled by the 'Root/Tip Mask' section. Similarly, all color-related adjustments, such as saturation and intensity, are also handled by the 'Root/Tip Color' section.*

*The necessary values ​​for Specular Lobe 1 and 2 are shown only if you want to experiment with brightness and reflections.*

*Scattering is simply adjusted in the 'Scatter' section to enhance the effects of light passing through the hair strands and improve the appearance of renders with integrated rim lights. For intense highlights, simply set 'Intensity' to values ​​above 0.600.*

*I will provide a more detailed manual later explaining its use and the function of each parameter.*

- C0ll3n DBD Hair (Legacy)
<img width="782" height="794" alt="image" src="https://github.com/user-attachments/assets/b6b22957-0932-411e-ad2b-73a376facd0f" />

*Legacy is quite different because it uses its textures independently, unlike IDGAD, which uses packaged textures. Therefore, it requires more textures to complete a setup.*

*The three main textures present in all Legacy hairs are Diffuse, Alpha, and Gradient (similar to a Mask or RootTip Mask), which I've grouped in the white area for this example. The textures that can sometimes exist are Height, ID, and Normal Map, which I've also enclosed in the blue area for the example. However, in the hair material information, we won't always have all compatible textures. For example, 'T_CMMHair_12_BC' can use the Normal Map 'T_CMMHair_03_Soft_N' without issue, as well as any texture that matches the same sample. That is, as long as the textures match in shape and strands (this can be determined simply by viewing the same textures in the Windows image viewer or the image viewer of your operating system), they can share the same textures. Unfortunately, materials don't always provide this information.*

*I'm keeping this in this function because the game relies heavily on the Unreal Engine to significantly improve real-time rendering without needing to create more physical strands. However, the render shows a "raw" model where we see the real model without any Unreal Engine shaders applied. Therefore, I'm working with this Blender shader in this way to compensate for these shortcomings, instead of integrating completely pure values ​​as Unreal Engine handles them.*

*And the Root and Tip Color options, which I put in the red group, are purely optional. They're simply the available inputs if you want to experiment with combining more colors and not just using Diffuse. Unfortunately, legacy textures are less detailed than IDGAD's, so I've included a checkbox to indicate whether or not you want to use them.*

*If Height and ID did not exist, I created a 'If Missing Maps' section where they can be procedurally derived, that is, based on existing main textures such as Diffuse, Alpha and Gradient.*

### Hair Composite Nodes

- C0ll3N Hair Composite
<img width="1031" height="693" alt="image" src="https://github.com/user-attachments/assets/61e9ba19-827b-4e26-b1fa-fc6ab5ff44fd" />

*These nodes are simply intermediaries that convert some parameters of the dedicated shader 'C0ll3n DBD Hair' for the Bubba and Lance Queen shaders, primarily. They can be used for other shaders as long as they accept similar essential inputs, at least from Diffuse and Alpha.*

*I don't see the need to explain texture connections here either, as they are handled the same way in the original shader.*

<img width="1051" height="817" alt="image" src="https://github.com/user-attachments/assets/a1849878-bf28-440f-a38e-863800bc8443" />

*For Lance Que's shader, you can connect 'Root Tip Mask' with 'Gradient Tint', although it's purely optional.*

<img width="1109" height="892" alt="image" src="https://github.com/user-attachments/assets/f5396756-d8b4-4f21-b57b-a3991853947e" />

*As I said before, the Legacy hair connections are the same as those used in the dedicated shader.*

<img width="1212" height="921" alt="image" src="https://github.com/user-attachments/assets/9c54d731-3889-4857-80fa-a421a6deca79" />

*The connections with the Lance Queen Legacy shader are a little different, as the Height Map must be connected to the Hair Composite as well as its shader.*

- C0ll3n HC Simple [IDGAD]

<img width="1134" height="619" alt="image" src="https://github.com/user-attachments/assets/e3ae2cab-efc8-4cf9-a65c-c34cd7792a33" />

*The simplified version also features adaptability sockets that can be used with both Bubba's and Lance Quen's IDGAD shaders, as well as their Legacy versions.*

*The question is: Are they necessary? This depends on your purpose in terms of appearance, as each shader works differently and is only similar in some aspects.*

### Parallax/Offset

- C0ll3n Parallax/Offset [Inputs & Outputs]
<img width="1403" height="783" alt="image" src="https://github.com/user-attachments/assets/05633675-e471-4ca1-b005-203381569f48" />

*These would be perhaps the most complex nodes to understand how they should be connected, but for this I created entries that adapt their function in DBD Hair and Hair Composite.*
