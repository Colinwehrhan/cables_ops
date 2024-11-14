 [Transform and Scale ops tutorial](https://www.youtube.com/watch?v=5pucC-GuDcs&list=PLYimpE2xWgBt8kR3H3Pk_U0PYqLrHNWf5&index=4)
- Putting multiple 3d assets below each other in a cable will cause inheritance
	- Cube1 scale with effect Cube2
	- Cube2 can scale independently if below Cube1 
- Optimizations
	- Scale is better to use instead of length, height, and width of meshes since that requires Cables to redraw the mesh
	- E.I. if you want to stretch a cube based on a sine wave you could time sine to render width, but using scale would be more performative

[Render to Texture](https://www.youtube.com/watch?v=4mWkws5fn5w&list=PLYimpE2xWgBt8kR3H3Pk_U0PYqLrHNWf5&index=6)
- render to texture - render a 3d scene into a 2d texture/image
- Takes a mesh or 3d scene an makes it into a 2d texture
	- Processes every single op below it 
	- That final result is then output as a texture
- If you have objects that are 3d use render to texture as image compose does not work
	
[Image compose op](https://www.youtube.com/watch?v=ZZKdaQw1bMo&list=PLYimpE2xWgBt8kR3H3Pk_U0PYqLrHNWf5&index=6)
- imagecompose - create texture/image using 2d effects/drawing 2d images
- Allows you to create or generate a texture and allows you to fill it with what you want
- Image compose generates an empty texture
	- Processes every single op below it 
	- That final result is then output as a texture as an texture from image compose
- Use for 2d scenes images etc.. so you only need image compose
- ==Optimizations==
	- Image compose by default uses the view port by default
	- Making the size smaller of imageCompose 512x512 will greatly increase performance

[Draw image](https://www.youtube.com/watch?v=Ww04Cw9wArM&list=PLYimpE2xWgBt8kR3H3Pk_U0PYqLrHNWf5&index=7)
- Use it most of the time to overlay one layer with another 
	- aka two images on top of each other
- Must be used with image compose op as image compose is looking for it

[Switch Trigger](https://www.youtube.com/watch?v=nCJO9yF7bnk&list=PLYimpE2xWgBt8kR3H3Pk_U0PYqLrHNWf5&index=8)
- Renamed to RouteTrigger
- Basic controlled by a number to switch

[Sequence Op](https://www.youtube.com/watch?v=1PtJG-Plz4Y&list=PLYimpE2xWgBt8kR3H3Pk_U0PYqLrHNWf5&index=9)
- The sequence renders from left to right
- right most will be rendered on top of the scene

[Repeat Op](https://www.youtube.com/watch?v=jiOLZaMUH78&list=PLYimpE2xWgBt8kR3H3Pk_U0PYqLrHNWf5&index=10)
- Repeats everything below it

[Random Numbers Op](https://www.youtube.com/watch?v=ASp7LEqZUIE&list=PLYimpE2xWgBt8kR3H3Pk_U0PYqLrHNWf5&index=12)
- random numbers can be used to generate values between a min and max
- by plugging in a timer to the seed input you can can a truly random seed
	- this makes the numbers random everytime

[Average interpolation Op](https://www.youtube.com/watch?v=iM3BTNHwmsA&list=PLYimpE2xWgBt8kR3H3Pk_U0PYqLrHNWf5&index=13)
- Renamed Ops.Anim.Smooth
- used to smooth out big jumps in values
- Good for smoothing out movements between positions

[Text Texture Op](https://www.youtube.com/watch?v=z1Qf9dE67-w&list=PLYimpE2xWgBt8kR3H3Pk_U0PYqLrHNWf5&index=15)
- Text is a texture that goes into a material

[Depth texture Op](https://www.youtube.com/watch?v=EzV5CRAMyTA&list=PLYimpE2xWgBt8kR3H3Pk_U0PYqLrHNWf5&index=16)
- This is an op to access the distance of the camera
	- Good for applying fade out on objects far in the horizion
- When using image compose with the depth texture you should select "add" or "subtract" to make depth lighting

[DepthTexture Focus](https://www.youtube.com/watch?v=x2iQhsX7P9k&list=PLYimpE2xWgBt8kR3H3Pk_U0PYqLrHNWf5&index=17)
- Can be used with textures depth texture output and image compose to create a blur
- You want to draw the full image, then apply a blur mask with as second image compose

[ArrayIterator](https://www.youtube.com/watch?v=63UbYklOZ3c&list=PLYimpE2xWgBt8kR3H3Pk_U0PYqLrHNWf5&index=19)
- Renamed to ArrayIteratorNumbers
- Good way to get numbers out of an array
- Performance wise it is looping over everything below it

[Set variable Op](https://www.youtube.com/watch?v=9__s5ukidmk&list=PLYimpE2xWgBt8kR3H3Pk_U0PYqLrHNWf5&index=20)
- Good way to clean up your patches

[Basic glow](https://www.youtube.com/watch?v=XmOk70epdf0&list=PLYimpE2xWgBt8kR3H3Pk_U0PYqLrHNWf5&index=21)
- Optimization
	- When creating effects like blur don't use view port size as it is very expensive

[Pixel displace op](https://www.youtube.com/watch?v=cc5Vlmvlq6A&list=PLYimpE2xWgBt8kR3H3Pk_U0PYqLrHNWf5&index=22)
- the brighter a pixel is the more that pixel gets displaced
- Can create really crazy effects when you layer it onto a wave form gradient

[Color area op](https://www.youtube.com/watch?v=cUU0fNw3rEg&list=PLYimpE2xWgBt8kR3H3Pk_U0PYqLrHNWf5&index=23)
- Colors an area emanating from a sphere, you can adjust its postition
- You can do it and X & Y to color an entire "plane"

[Tips & tricks 1](https://www.youtube.com/watch?v=AE4_XIpmS3Y&list=PLYimpE2xWgBt8kR3H3Pk_U0PYqLrHNWf5&index=24)
- crtl + p 
	- render, can change rendre size
	- scale, can scale the render
- c, brings you to center

[Ease op](https://www.youtube.com/watch?v=PEVSinWoOSc&list=PLYimpE2xWgBt8kR3H3Pk_U0PYqLrHNWf5&index=25)
- Super useful when working with moving objects
	- map min/max for it to work
- Good to use with modulo
	- has tons of easing effects

[Vertex displacement op](https://www.youtube.com/watch?v=NjG85Qbbl0w&list=PLYimpE2xWgBt8kR3H3Pk_U0PYqLrHNWf5&index=26)
- displace the vertices of the mesh depending on brightness of the pixels of a texture
	- Adding more vertices to your shape does cost compute though
- Used in tandem with noise filters

[PointMaterial and PointCloudFromArray](https://www.youtube.com/watch?v=tFM2Ixf-ixs&list=PLYimpE2xWgBt8kR3H3Pk_U0PYqLrHNWf5&index=27)
- Point material controls the size
	- if you are zooming in be sure to check the "Scale by distance"

[IfTureThen op](https://www.youtube.com/watch?v=3dYztfuw4lA&list=PLYimpE2xWgBt8kR3H3Pk_U0PYqLrHNWf5&index=28)
- Pretty basic 
- good for random cluster to make two different objects without having two renders

[GeometryPoints op](https://www.youtube.com/watch?v=-X93M13KodM&list=PLYimpE2xWgBt8kR3H3Pk_U0PYqLrHNWf5&index=29)
- Can grab the vetrices of a rendered shape
	- use it to draw only once
- Then draw splines or points from vertexs

[PointsFeild3d op](https://www.youtube.com/watch?v=tVphEMCXDb4&list=PLYimpE2xWgBt8kR3H3Pk_U0PYqLrHNWf5&index=30)
- Now called PointsCube
- Good for making quick grids of mesh instances 

[Bool anim op](https://www.youtube.com/watch?v=BzYl9lujqmg&list=PLYimpE2xWgBt8kR3H3Pk_U0PYqLrHNWf5&index=31)
- good for animating between states
	- changing shapes or brining things in an out of frame
	- think powerpoint animations
- has automatic easing

[Pixel projection](https://www.youtube.com/watch?v=xkIrVtSU4FU&list=PLYimpE2xWgBt8kR3H3Pk_U0PYqLrHNWf5&index=32)
- changes the coordinate system for the ops below it to pixels
	- this works for 2d textures
- This makes it so you can resize and the object stays locked in the same pixel position
- For 3d use screen coordiantes

[Transform vertex op](https://www.youtube.com/watch?v=SaKWF6RnsyI&list=PLYimpE2xWgBt8kR3H3Pk_U0PYqLrHNWf5&index=36)
- Really really good for spinning or transforming large instances of meshes
- uses GPU not CPU so it can use a lot more points
