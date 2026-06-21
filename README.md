# C0ll3n-DBD-Nodes

## Content
### Dedicated Shaders

*These are dedicated hair shaders that expect IDGAD (packaged) or Legacy texture inputs for the hair*

- C0ll3n DBD Hair [IDGAD]
- C0ll3n DBD Hair [Legacy]

<img width="600" height="709" alt="v2 3 Info2" src="https://github.com/user-attachments/assets/5e0cc6a3-bda5-4494-b3ac-387f05e5867e" />

### Hair Composite Nodes

*These are nodes that attempt to convert certain parameters from the dedicated shaders to the Bubba or Lance Queen shaders*

- C0ll3n HC IDGAD
- C0ll3n HC Legacy
- C0llen HC Simple [IDGAD]

<img width="884" height="812" alt="v2 3 Info1" src="https://github.com/user-attachments/assets/bbe3c0b4-f73e-4906-bcf9-1b875749176d" />

### Custom Hairs shader and node

*The IDGAD Hairs node group must be connected to one of the shaders that accept IDGAD texture inputs; it can be used with any shader that processes these textures. Hair Styles is a standalone shader that offers more features because it uses more textures than IDGAD can provide on its own, even with the Flow map*
*Requires to remap the UV's using a Hair Guide texture (Included in the blend file) in UV Editor*

- C0ll3n IDGAD Hairs
- C0ll3n Hair Styles

<img width="527" height="434" alt="v2 3 Info4" src="https://github.com/user-attachments/assets/497d693c-1ee1-4d67-9741-af7ba5fc09f2" />

### Parallax/Offset Alpha Hair Composite, Input and Output

*These are groups of nodes designed to create the effect of adding more hair, which is useful for models with very little hair. The effect varies depending on the viewing angle, but it requires support from a shader; it can be either IDGAD or Legacy, and there is a version for each*
*You need to create 3 more copies of the original texture, depending on which one you're working on (IDGAD or Legacy), no apply for Simple version*

- C0ll3n IDGAD AHC [I(P/O)]
- C0ll3n IDGAD AHC [O(P/O)]
- C0ll3n Legacy AHC [I(P/O)]
- C0ll3n Legacy AHC [O(P/O)]
- C0ll3n Simple Parallax

<img width="773" height="446" alt="v2 3 Info3" src="https://github.com/user-attachments/assets/5042469b-5cde-48f6-804b-1b47a6fc9b27" />

### Extras node groups

*These are groups of nodes that function as additional add-ons: “Sun Damage” adds a gradient to “DBD Face Sun Damage” within Bubba's nodes, leaving a visible mark along the edges; “Texture Color Influence” is only for editing colors, saturations, etc., of a color texture (BC); “Custom Tip/Root Color” is only useful on hair whose UVs' have been changed—such as Legacy wigs—to use IDGAD shaders or the dedicated Hair Styles shader, and "DBD JD IDGAD" is a group of nodes that only work for Bubba shaders that expect those inputs (Specular, Roughness, and Scatter)*

- Sun Damage Gradient
- Texture Color Influence
- Custom Tip/Root Color
- DBD JD IDGAD

<img width="782" height="329" alt="v2 3 Info5" src="https://github.com/user-attachments/assets/20ddca96-6133-41c4-94ca-af36cf00f9fc" />

### Hair Guides

*These are alpha textures for use it as a guide designed to can be applied with custom hairs node and/or shader, it's for remap (Swap) your hair models, this process can be done in UV Editing in Blender; for being append, you have to go in 'Image' folder; HairGuide_IRS it's a texture made for IRS texture made from Bubba, but it needs to be imported maually (IRS.png inside 'Image' folder) using a 'Texture Image' node and connect it in any IDGAD shader*

<img width="132" height="242" alt="v2 3 SS3" src="https://github.com/user-attachments/assets/744508a9-e7c3-4845-9a03-2fb18e32b5e9" /> <img width="167" height="99" alt="v2 3 SS4" src="https://github.com/user-attachments/assets/eeddfb1c-14b3-4e14-aeb3-a08387706cae" />
