```cpp
// Blending 
glEnable(GL_BLEND);
glBlendFunc(GL_SRC_ALPHA, GL_ONE_MINUS_SRC_ALPHA);
glBendEquation(); // DEFAULT is GL_FUNC_ADD
```


---

### glBlendFunc(src, dest)
- `glBlendFunc(src, dest)` will specify the values with the *src* and *destination's* RGBA will be multiplied 
- **GL_SRC_ALPHA** will be = 0, if the pixel should be transluscent (for png images)
	- src = 0
- **GL_ONE_MINUS_SRC_ALPHA** 
	- dest = 1 - 0 = 1
- this means "use the destination color" (color that's alredy in the buffer)
- the following operation will be made for each RGBA value:
	- $R=(r_{src} \cdot 0 ) + (r_{dest} \cdot (1-0))=r_{dest}$ 


### glBlendEquation(mode)
- mode will specify how *src and dest values* are combined
- Default vale is GL_FUNC_ADD
- 