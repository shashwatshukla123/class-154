# class-154

To create a ring target element through the component, we first need to register it in A-Frame. To create a new element, JavaScript DOM provides us a predefined function called createElement()

which will help create the new entity. Using the setAttribute() method, we'll set attributes of the rings like material color and its geometry to the ring.

A component with one property value is a single property component, and multiple property values have many values as properties of the component.

We want to set the color property with the color value for the material component. But for the geometry component, we want to set the primitive shape as a torus and the radius of the shape, which will be written as a JSON object.

rings:
Let’s use the .init() method, which is loaded as soon as the component is attached to the entity, to write this for loop. Let's make 20 rings. Each ring that we create needs to have a unique id; to assign this unique id; we can use the counter value of the loop.

We can manipulate the string to generate a unique id by using template literal ${} to join strings. We also need to have different positions for each ring.

use the random function to generate a random number.

In JavaScript, the Math.random() function gives the values between 0 and 1. We can multiply the random number with a number to get the value between any other numbers. For example, Math.random()*100 will give random values between 0 and 100.

We can also add and subtract to get the different range of numbers. For example, Math.random()*100 + (-50) will give random values between -50 and 50.

we can attach this entity to any of the elements in the scene. Let’s make the rings a child of the terrain element.

Inside the function, we'll first select the terrain using the JavaScript DOM function document.querySelector() using the id given to the terrain element. querySelector() function helps to select the particular entity element once the id is given to the entities.

Now, to make the ring entities child of the terrain entity, add the ring entities as the child of the terrain using terrainEl.appendChild(ringEl). appendChild() is also the JavaScript DOM function that can be used to make one element a child of another element.

birds:
The approach for creating the birds will remain the same.

We will first create the element. Here, instead of setting geometry and material, we can set the gltf model that's already loaded. Then we can add this bird element to the scene using querySelector() and appendChild().

Finally, we can create multiple elements by calling the create function in a for loop. Here we can generate unique ids and positions of elements.

animation-mixer component:
the birds that we would see in the simulation would be static and we want the birds to be animated.

In the setAttribute() method we'll use the animation-mixer component. With the help of this component, we can activate the animation of the model. This component is a part of another library of A-Frame - “aframe-extras”.

The animation-mixer component of this library has many properties which we will explore later. For now, we can just use the empty JSON object to keep the default values of any component.



