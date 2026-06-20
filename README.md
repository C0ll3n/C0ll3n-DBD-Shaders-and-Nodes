# C0ll3n-DBD-Nodes

## Content
### Dedicated Shaders

*These are dedicated hair shaders that expect IDGAD (packaged) or Legacy texture inputs for the hair*

- C0ll3n DBD Hair [IDGAD]
- C0ll3n DBD Hair [Legacy]

### Hair Composite Nodes

*These are nodes that attempt to convert certain parameters from the dedicated shaders to the Bubba or Lance Queen shaders*

- C0ll3n HC IDGAD
- C0ll3n HC Legacy
- C0llen HC Simple [IDGAD]

### Custom Hairs shader and node

*The IDGAD Hairs node group must be connected to one of the shaders that accept IDGAD texture inputs; it can be used with any shader that processes these textures. Hair Styles is a standalone shader that offers more features because it uses more textures than IDGAD can provide on its own, even with the Flow map*
*Requires to remap the UV's using a Hair Guide texture (Included in the blend file) in UV Editor*

- C0ll3n IDGAD Hairs
- C0ll3n Hair Styles

### Parallax/Offset Alpha Hair Composite, Input and Output

*These are groups of nodes designed to create the effect of adding more hair, which is useful for models with very little hair. The effect varies depending on the viewing angle, but it requires support from a shader; it can be either IDGAD or Legacy, and there is a version for each*
*You need to create 3 more copies of the original texture, depending on which one you're working on (IDGAD or Legacy), no apply for Simple version*

- C0ll3n IDGAD AHC [I(P/O)]
- C0ll3n IDGAD AHC [O(P/O)]
- C0ll3n Legacy AHC [I(P/O)]
- C0ll3n Legacy AHC [O(P/O)]
- C0ll3n Simple Parallax

### Extras node groups

