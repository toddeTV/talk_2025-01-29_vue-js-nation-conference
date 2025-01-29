---
layout: basic
---

# glTF type generation - Implementation

<v-clicks>

- run `three.js` in node dev and pipe model into it, we then get the runtime object
  - <ant-design-smile-filled class="text-green-400" /> No own parsing
  - <ant-design-smile-filled class="text-green-400" /> Exact what the user gets when they load the model in their runtime
- generate types out of the runtime object by taking the names of all children
- store scene graph paths with the child indices linked to the child names
- use handlebars to generate files
- we generate:
  ```diff
   @/assets/models/Island.gltf
   @/assets/models/Island.bin
   @/assets/models/Island-texture1.png
   @/assets/models/Island-texture2.png
  +@/assets/models/Island.gltf.d.ts      <- the typing
  +@/assets/models/Island.gltf.js        <- actual code with node get helper function and model graph representation
  ```

</v-clicks>
