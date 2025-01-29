---
layout: two-cols
---

# load a glTF file

::left::

## ThreeJS (native)

````md magic-move {lines: true}
```js {*}
const loader = new GLTFLoader();

// loader.setDRACOLoader(dracoLoader);   <- optional

loader.load(
  '//localhost:3000/models/Island.gltf',
  function ( gltf ) { // on success
        // do something ...
    scene.add( gltf.scene );
    gltf.animations; // Array<THREE.AnimationClip>
    gltf.scene; // THREE.Group
    gltf.scenes; // Array<THREE.Group>
    gltf.cameras; // Array<THREE.Camera>
    gltf.asset; // Object
  },
  function ( xhr ) { // while loading
        const per = xhr.loaded / xhr.total * 100;
    console.log( per + '% loaded' );
  },
  function ( error ) { // on error
    console.log( 'An error happened' );
  }
);
```
````

::right::

## TresJS (Vue/ Nuxt)

````md magic-move {lines: true}
```vue {*}
<script setup lang="ts">
import { OrbitControls, useGLTF } from '@tresjs/cientos'
import { TresCanvas } from '@tresjs/core'
const path = '//localhost:3000/models/Island.gltf'
const { scene: modelScene } = await useGLTF(path, {
    // draco: true   <- optional
})
</script>

<template>
  <TresCanvas>
    <Suspense>
      <primitive :object="modelScene" />
    </Suspense>
  </TresCanvas>
</template>
```
````
