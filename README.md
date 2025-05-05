# computer-graphics-assignment-2--ray-tracing-solved
**TO GET THIS SOLUTION VISIT:** [Computer Graphics Assignment 2 -Ray Tracing Solved](https://www.ankitcodinghub.com/product/computer-graphics-assignment-2-ray-tracing-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;99804&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;Computer Graphics Assignment 2 -Ray Tracing Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
&nbsp;

1 Introduction

In this exercise you will implement a basic ray tracer. A ray tracer shoots rays from the observer’s eye (the camera) through a screen and into a scene which contains one or more surfaces. it calculates the rays intersection with the surfaces, finds the nearest intersection and calculates the color of the surface according to its material and lighting conditions. You are required to implement a ray tracer with the following features. Please read the complete document carefully before you start coding!

2 Surfaces

• Spheres. Each sphere is defined by the position of its center and its radius.

• Infinite planes. Each plane is defined by its normal N and an offset c along the normal. A point P on the plane will satisfy the formula P ·N = c.

• Cubes. Each cube is defined by the position of its center (x, y, z) and its edge length (scalar). All boxes are axis aligned (meaning no rotations) to make the computation of intersections easier.

3 Materials

To compute the color of a surface, you have to take into consideration the object’s material. If the material is reflective, you need to shoot reflection rays to find objects which would be reflected. If the material is transparent or semi- transparent, you need to shoot rays through the surface to find objects that are behind it. Each rendered surface (sphere or plane) is associated with a material in the scene file. Several surfaces can be associated with the same material. Each material have the following attributes:

• Diffuse color (RGB). This is the ”regular” color of a surface. This value is multiplied by the light received by the object to find the base color of the object.

1

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
<ul>
<li>Specular color (RGB). Specularity is the reflection of a light source. The specular color of a surface defines the intensity and color of that reflection. Materials in real life often have different specular color than diffuse color. For example, a polished wooden desk would have a brown diffuse color but white specular color.</li>
<li>Phong specularity coefficient (floating point number). We will use the Phong shading model. This coefficient controls the type of specularity of a surface. A high value (around 100) renders small and sharp specular reflections, for shiny surfaces such as metal, and a low value (around 1 or so) renders wide and soft specular reflections, for materials such as clay or stone.</li>
<li>Reflection color (RGB). Reflections from the surface are multiplied by this value. For example a red metal pipe might reflect its surrounding but the reflection will have a red tint.</li>
<li>Transparency (floating point number). This value will be 0 when the material is opaque (not transparent at all) and 1 when the material is completely transparent. Note that a surface can be completely transparent and still show reflections of the surfaces which surround it (the reflections are independent of the object’s transparency).
4 Lights

To light the scene we will use point lights. Point lights are located at a certain point and shoot light equally in all directions around that point. You will also have to implement soft shadows, as explained later. Each light will have the following attributes:
</li>
</ul>
<ul>
<li>Position (XYZ). A vector specifying the position of the point light.</li>
<li>Color (RGB).The color of the light. This color multiplies (RGB element wise) the surface diffuse and specular colors when the surface is lit by this light.</li>
<li>Specular intensity (floating point number). Sometimes we would like a light to produce only diffuse lighting, or only partial specular light- ing. If this number is 1, the light intensity will be the same for the diffuse component and the specular component computation. Otherwise, the light color will be multiplied by the specular intensity for the specular compo- nent computation.</li>
<li>Shadow intensity (floating point number). Usually when lighting a scene there will be a key light which is casting a strong shadow, and some other lights (like fill light or rim light) which does not cast shadows. Sometimes we would also like a light to partially go through surfaces and light their background as well, to reduce the necessary number of lights to
2
</li>
</ul>
</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
5

</div>
</div>
<div class="layoutArea">
<div class="column">
•

</div>
<div class="column">
light a scene. The light received by a surface which is hidden from the light is multiplied by (1-shadow intensity). In other words, If this number is 1, the light casts full shadows so no light will be received by the obscured surface (from this particular light source). If this number is 0, the light casts no shadows at all (the lighting is the same whether the surface is obscured from the light or not). For values in the range between 0 and 1, the light will cast a partial shadow. Note that in this case the shadow intensity is not accumulated; it doesn’t matter how many objects are in the way between the light source and the surface, it is either obscured with partial shadow or it is fully lit.

Light Radius (floating point number). This value is used to compute soft shadows, see description below.

Camera and Genral Settings

</div>
</div>
<div class="layoutArea">
<div class="column">
The camera is defined by the following attributes. There will be only one camera in each scene file.

<ul>
<li>Position (XYZ). A vector specifying the position of the camera.</li>
<li>Look-at point (XYZ). A vector specifying the point the camera is look- ing at. When defining a scene, it is simpler to work with look-at points than specifying a direction. In your code you have to compute the direc- tion of the camera from the look-at point and the camera position.</li>
<li>Up vector (XYZ). The up vector of the camera defines the direction the camera is looking up at. For convenience, this vector is not necessary perpendicular to the direction vector of the camera. In your code you have to fix the up vector so it is perpendicular to the direction vector you computed from the look-at point.</li>
<li>Screen distance (floating point number). The distance of the camera’s screen from the camera. This value defines the focal point of the camera, and controls the direction of the ray that will go through each pixel.</li>
<li>Screen width (floating point number). The width of the camera’s screen. Together with the screen distance, this value controls the viewing angle of the camera. When the screen is wider or the distance is shorter, the camera’s viewing angle is larger. The screen height is computed using the requested aspect ratio of the image and this number. A screen dis- tance roughly equal to the diagonal of the screen size produces a ”normal” camera lens, similar to the camera in your phone.
There are also some general settings that are used to describe a scene.

• Background color (RGB). This color is used when a ray does not hit any surface. Note that reflection rays and transparency rays also use this background color when they do not hit another surface.

3
</li>
</ul>
</div>
</div>
</div>
<div class="page" title="Page 4">
<div class="layoutArea">
<div class="column">
<ul>
<li>Number of shadow rays (small integer, 1−10). This number controls the amount of rays which are used for every light to compute soft shadows. Note that shadow rays are emitted from a squared area N*N, so if this number is for example 5 there will be 25 rays emitted for each shadow calculation.</li>
<li>Maximum recursion level (integer, usually around 10). Since reflective surfaces can reflect other reflective surfaces and so on, each time the re- flection color is computed there is a recursion. This number limits the recursion level, so after this amount of recursion the returned color would be the background color (as if the tenth reflected surface does not exist).
6 Tips

This section will give a general overview of ray tracing as a reminder to what you saw in class.
</li>
</ul>
6.1 General Process

The general process of ray tracing is:

<ol>
<li>Shoot a ray through each pixel in the image. For each pixel, you should:
<ol>
<li>1.1. &nbsp;Discover the location of the pixel on the camera’s screen (using cam- era parameters).</li>
<li>1.2. &nbsp;Construct a ray from the camera through that pixel.</li>
</ol>
</li>
<li>Check the intersection of the ray with all surfaces in the scene (you can add optimizations such as BSP trees if you wish but they are not mandatory).</li>
<li>Find the nearest intersection of the ray. This is the surface that will be seen in the image.</li>
<li>Compute the color of the surface:
<ol>
<li>4.1. &nbsp;Go over each light in the scene.</li>
<li>4.2. &nbsp;Add the value it induces on the surface.</li>
</ol>
</li>
<li>Find out whether the light hits the surface or not:
<ol>
<li>5.1. &nbsp;Shoot rays from the light towards the surface</li>
<li>5.2. &nbsp;Find whether the ray intersects any other surfaces before the required surface – if so, the surface is occluded from the light and the light does not affect it (or partially affects it because of the shadow intensity parameter).
4
</li>
</ol>
</li>
</ol>
</div>
</div>
</div>
<div class="page" title="Page 5">
<div class="layoutArea">
<div class="column">
6. Produce soft shadows, as explained below:

6.1. Shoot several rays from the proximity of the light to the surface. 6.2. Find out how many of them hit the required surface.

6.2 Additive Colors

A short reminder about additive colors: The output color of the surface is the sum of its diffuse color, its specular color and its reflective color.

If a surface is transparent, objects behind the surface should be ray traced to discover the color (by shooting the same ray from the camera and checking what is the next surface the ray hits). The following formula will then be used:

output color = (background color) · transparency +(dif f use + specular) · (1 − transparency) +(reflection color)

In other words, the reflection color is added after the transparency of the object (otherwise we could not have strong reflections on transparent objects which is very common in real life – think of the a soap bubble).

6.3 Math

Use cross products to generate vectors which are perpendicular to a plane. To find a plane that is perpendicular to a vector, find a perpendicular vector (this should be easy!) and then find the third vector by using a cross product. You can also use the cross products to fix the up vector of the camera.

To render boxes, you can use the slabs method (look it up…). Basically it means that you find the six planes around the box (two for each axis), and then check the order in which the ray hits the planes. If the first three planes that are hit are from three different axes, then the ray hits the box and the first plane that was hit determines the normal and position of the hit point. If two parallel planes are hit before the planes of other axis are hit, the ray does not hit the box.

7 Soft Shadows

There are several methods to compute soft shadows. We will implement one method which produces nice results but is somewhat computationally heavy. The submitted solution should follow the method here.

In general, to generate shadows on a surface we will send a ray from the light source to the surface and check whether the ray hits other objects prior to that surface. This will produce a hard shadow, as every pixel would either be

5

</div>
</div>
</div>
<div class="page" title="Page 6">
<div class="layoutArea">
<div class="column">
completely lit or completely shadowed. In reality lights do not emanate from points, because the light source has some area to it.

To generate soft shadows, we will send several shadow rays from the light source to a point on the surface. The light intensity that hits the surface from this light source will be multiplied by the number of rays that hit the surface divided by the total number of rays we sent. For example, if we send 25 rays from the light source and 5 of them hit the surface at the given point, the surface will be 20% illuminated at that point. If the number of shadow rays parameter is 1 only one ray will be cast and the shadows will be hard.

The sent rays should simulate a light which has a certain area. Each light is defined with a light radius (see light parameters). To simulate a light with a radius we use the following process:

<ul>
<li>Find a plane which is perpendicular to the ray.</li>
<li>Define a rectangle on that plane, centered at the light source and as wide
as the defined light radius.
</li>
<li>Divide the rectangle into a grid of N*N cells, where N is the number of shadow rays from the scene parameters.</li>
<li>If we shoot a ray from the center of each cell, we will get banding arti- facts (you can test it and see for yourself). To avoid banding we select a random point in each cell (by uniformly sampling x value and y value using rnd.nextDouble() function), and shoot the ray from the selected random point to the light.</li>
<li>Aggregate the values of all rays that were cast and count how many of them hit the required point on the surface.
Note that this process is done for every point on the surface that we look at (or every camera ray, reflection ray or transparency ray that we shoot).

lastly:

light intesity = (1 − shadow intensity) ∗ 1 +shadow intensity ∗ (% of rays that hit the points f rom the light source)

7.1 Bonus

With this method we didn’t account for transparency of the objects on the way from the light source to the point. Actually, if the objects on the way are somewhat transparent, some light can go through and reach the point.

Each pair that will account for the objects on the way using their transparency values in the shadow calculation, will get a 5 point bonus.

6
</li>
</ul>
</div>
</div>
</div>
<div class="page" title="Page 7">
<div class="layoutArea">
<div class="column">
8 Implementation Details

The ray tracer should be implemented in Python. To define a scene to render, the input for the ray tracer will be a scene file which is a simple text file that defines every surface, material and light source in the scene, as well as some camera settings and general settings for the render.

The code should run in the command line (you need to send a directory with all the python code files) and accept 4 parameters. For example:

python RayTracer.py scenes\Spheres.txt scenes\Spheres.png 500 500 The first parameter is the scene file, and the second is the name of the image file to write. Those two are mandatory. The next two parameters are optional and define the image width and height, respectively. Please set the default size to 500 × 500.

The scene description file is described below. Several scene files will be uploaded along with the images they should produce. Please also perform tests on other scene files that you write yourself. Your code will be tested on several other scene files as well to make sure it works correctly for all cases.

There is no need for optimizations (such as BSP trees etc).

8.1 Bonus

We will give bonus points for submissions with fast implementation. Optimize your code so it will be as fast as possible. The bonus will be given to the top-k performing submissions (k will be determined later).

9 Scene Definition Format

The scenes are defined in text scene files with the following format.

Every line in the file defines a single object in the scene, and starts with a 3 letter code that identifies the object type. After the 3 letter code a list of nu- meric parameters is given. The parameters can be delimited by any number of white space characters, and are parsed according to the specific order in which they appear. Empty lines are discarded, and so are lines which begin with the character ”#” which are used for remarks. The possible objects with their code and list of required parameters are given below.

<pre>"cam" = camera settings (there will be only one per scene file)
params[0,1,2] = position (x, y, z) of the camera
params[3,4,5] = look-at position (x, y, z) of the camera
params[6,7,8] = up vector (x, y, z) of the camera
</pre>
<pre>params[9] = screen distance from camera
params[10] = screen width from camera
</pre>
<pre>"set" = general settings for the scene (once per scene file)
params[0,1,2] = background color (r, g, b)
</pre>
7

</div>
</div>
</div>
<div class="page" title="Page 8">
<div class="layoutArea">
<div class="column">
params[3] = root number of shadow rays (N2 rays will be shot) params[4] = maximum number of recursions

<pre>"mtl" = defines a new material
params[0,1,2] = diffuse color (r, g, b)
params[3,4,5] = specular color (r, g, b)
params[6,7,8] = reflection color (r, g, b)
params[9] = phong specularity coefficient (shininess)
params[10] = transparency value between 0 and 1
</pre>
<pre>"sph" = defines a new sphere
params[0,1,2] = position of the sphere center (x, y, z)
params[3] = radius
params[4] = material index (integer).  each defined material gets an
automatic material index starting from 1, 2 and so on
</pre>
<pre>"pln" = defines a new plane
params[0,1,2] = normal (x, y, z)
params[3] = offset
params[4] = material index
</pre>
<pre>"box" = defines a new box
params[0,1,2] = position of the box center (x, y, z)
params[3] = scale of the box, length of each edge
params[4] = material index
</pre>
<pre>"lgt" = defines a new light
params[0,1,2] = position of the light (x, y, z)
params[3,4,5] = light color (r, g, b)
params[6] = specular intensity
params[7] = shadow intensity
params[8] = light width / radius (used for soft shadows)
</pre>
10 Submission Guidelines

<ul>
<li>Submission is in pairs.</li>
<li>Submit your zip file through the Moodle site of the course.</li>
<li>Submit .zip file titled ex1 ⟨id1⟩ ⟨id2⟩ .zip, where ⟨id1⟩ and ⟨id2⟩ are your ids.</li>
<li>The zip should include the rendering results of the provided scenes with the same names .png plus an original scene named ”original.png”.
8
</li>
</ul>
</div>
</div>
</div>
