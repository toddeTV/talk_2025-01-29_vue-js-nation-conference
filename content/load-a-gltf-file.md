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
	'//localhost:3000/models/windmill.gltf',
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
const path = '//localhost:3000/models/windmill.gltf'
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

<div class="mt-4 w-full">
    <div
        class="w-70 flex flex-col gap-1 px-1 py-2"
        v-click="1"
        v-mark="{ at: 1, color: '#ab2657', type: 'box' }"
    >
        <div>
            loads at runtime
        </div>
        <div class="complementaryColor">
            <mdi:do-not-disturb-alt class="mr-2"/> no typings
        </div>
        <ul class="complementaryColor pl-8">
            <li>no code completion</li>
            <li>no safeguarding on build</li>
        </ul>
    </div>
</div>
