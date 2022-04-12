# 161


We know that A-Frame is built on Three.js. We need to see how we can access any object or function present in Three.js using A-Frame.
A-Frame’s <a-scene> is mapped with a Three.js scene.
A-Frame’s <a-entity> is mapped to one or more Three.js objects.
The Three.js scene is accessible from the <a-scene> element as .object3D.
  
  
 to access the Three.js scene we can use: document.querySelector('a-scene'). object3D
Every A-Frame entity (<a-entity>) has its own THREE.Object3D. 
 To access entity as the Three.js object we can use: document.querySelector('a-entity'). object3D
  
  
  Let’s get the camera entity as the Three.js object using: document.querySelector('#camera').o bject3D
Now, to define the Three.js vector, we need to create Three.js vector objects using “new THREE.Vector3()”.
We can create a variable direction to create a new Three.js vector object.
Now, to get the direction of the camera element we can use the .getWorldDirection(vectorVariable) method defined in Three.js.
camera.getWorldDirection(direction), will set the value of the vector given by the method in the direction variable.
Let’s check the value of direction using console.log(direction).
  
  
  click and drag the mouse to change the direction of the camera and check the result in the console.
We can see that as we move the camera, the value of direction changes.
To increase the bullet speed, we can multiply the direction vector with a number using multiplyScalar().
We will be using the negative number in the direction going into the screen.
Now let’s test the output. We can see that the bullet always goes in the camera direction.
  
  Now that we have learned how to create custom components and use them in the A-Frame scene, it's your turn.
  
  
  We have learned how we can use Three.js to get the camera direction to set the bullet's shooting direction.
  ***********************************************
Now  add the shooting gun model and write a component to shoot the bullet out of the model
  
  add the gLTF model of the gun shooter in the scene as the child entity of the camera and test the output.
  
  add in index .html
  
  assets  and add the gltf id for the entity
