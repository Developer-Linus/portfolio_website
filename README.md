# Theory
## Dimensions
- allow us to define the space surrounding us.
- Types:
1. Zeroth dimension (OD)—a point without dimension.
2. First dimension (1D)—a line with no width and height.
3. Second dimension(2D)—shape with length and width with no depth.
4. Third dimension (3D)—shape with lenght, width, and height. These three gives a volume.
5. Fourth dimension (4D)—This is time. Used alongside length, width, and height.
--
# What is Three.js?
- It is a JavaScript library and an API built on top of WebGL enabling us to create 3D graphics.
- Three.js enable us to create environment and scene where we can create interactions for our 3D objects.
- We should not confuse `scene` and `environment`. The Scene is the overall container while environment is the surrounding 
atmosphere or backdrop within the scene. 
- We make a scene our own world with the help of `objects`.
- Objects are the building blocks of a 3D scene.
- Once we have objects in our scene, we have to make them interactive. This is where the concept of `animations` come in.
- `Animations` involve transforming objects' positions or change its size or angle through rotation.
- To make animations even more realistic, Three.js allows us to add `shadows` and `lights`.
- In 3D world, we have `cameras` that act as our eyes in the real-world.
- Cameras in 3D scene decide parts the user will see in the scene.
> Now the question is, what we do with the information that our eyes give us?
- They are passed to our brains for processing.
- `Renderer` is the brain in Three.js.
- It processes everything defined to produce the output.
--
# 3D Objects
- Anything you can see or interact with in a 3D scene.
- Types:
1. `Mesh` (common object)—formed by combining `geometry` and `material`.
2. `Points` - collection of small dots in a 3D space. Used for creating stars or particles.
3. `Line` - represents connection between two points in a 3D space.
4. `Group` - collection of multiple objects.
5. `Sprite` - object that always faces the camera.

> Like the JavaScript where everything is an object inheriting from a base class, objects in Three.js inherit from `Object3D`.
--
# Position
- Where an object is located in a 3D scene.
- Defined by x, y, and z indices.
- x moves object left or right.
- y moves object up or down.
- z moves object closer or further away from you.
--
# Rotation
- How an object is turned or spun in a 3D space.
- You can rotate along x, y, or z axes.
--
# Scale
- Refers to how small or big an object is.
- You can scale based on x, y, or z axes.
-- 
# Mesh
- Core 3D object.
- Imagine it as a physical object.
- It can be a simple 3D geometric shapes provided by Three.js or models created by mering various 3D shapes.
- Made up of 2 main parts: `geometry` and `material`.
## Geometry
- Defines the shape or structure of a 3D object.
- Explained by three properties: `vertices`, `edges`, and `faces`.
- `Vertices` are the corner points or positions in a 3D space.
- `Edges` meet at vertices.
- Vertices are points in space defined by its co-ordinates (x,y,z).
- Edge connect two vertices.
- Edges outline the shape of the object.
- `Faces` are flat surfaces that connect vertices to form the geometry of the shape.
> Another important aspect in 3D world is a `triangle`.
- Everything in the 3D world is made up of triangles.
- Look at `Box Geometry`.
- You can create `custom geometry`.
-- 
## Material
- Determines how the surface of geometry looks.
- Defines the color, texture, transparency, shininess, and how light interacts with the mesh.
- It is like the skin of the 3D object.
- `Visual effect` I want to achieve determines the material I want to use. Check the documentation.
- `Texture` is an image in Three.js. It is like `png`, `jpeg`, and `gif` or a pattern applied to the surface of a 3D pattern.
--
> Now we have created a `Mesh`, an object, but they are in dark. How can we see them?
> Let there be `LIGHT`
# Light
- Illuminates the 3D scene. 
- Types:
1. AmbientLight—provides uniform lighting to all objects in the scene without casting shadows.
2. PointLight—emits light from a single point  in all directions. 
3. DirectionLight—simulates parallel light rays coming from a specific direction.
4. SpotLight—emits light rays in a con-shaped similar to a flashlight.
5. HemisphereLight - provides lighting from above and below the scene simulating light from the sky.
--
# Camera
- Everything we see in the 3D space comes from a camera perspective.
- Determines the view of the 3D scene.
- No camera, no objects in 3D scene because there is no viewpoint from which to observe them.
- Types:
1. `Perspective Camera`: mimics how human eyes see the world. Objects near camera are larger and vice versa. Called `Perspective Projection`.
2. `Orthographic Camera`: Removes the perspective effect. Objects are of similar size irrespective of how far they are from the camera. This is called `orthographic projection`.
3. `Stereo Camera`: Creates two views of the scene. One for the right eye and one for the left eye. Simulates 3D depth.
> Properties of camera are key in understanding the working of camera.
1. `Field of View (FOV)`- extent of the observable world visible through the camera at any moment. The angle you set determine the field of view in a scene.
2. `Point of View (POV)` - all about camera position and direction. Where are you looking from?
3. `Aspect Ratio` - ratio of width to height of camera's view.
4. `Near and Far Clipping Planes` - defines the boundaries of the camera view. `Near clipping plane` is the closest distance from the camera. Any object closer to camera than this distance will not be rendered.
`Far clipping plane` is the farthest distance from the camera at which objects are visible. Objects at distance beyond this will not be rendered.
--
# Controls
- Camera controls enable us to interact with camera dynamically using mouse or touch inputs.
- Types in Three.js:
1. `OrbitControls`(common)- used for interacting with an object from all angles. Used in Apple website for interacting with the products.
2. `TrackballControls`-offers more flexibility. No fixation.
3. `FlyControls`- it acts as if user is flying through the scenes.
4. `PointerLockControl`- Locks the cursor on the screen and allows the user to look around as if they were in the scene themselves.
5. `FirstPersonContorls`-camera moves in the direction the user is facing.
