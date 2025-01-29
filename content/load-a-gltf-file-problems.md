---
layout: basic
---

# load a glTF file - Problems

<v-clicks>

- <mdi-code class="mr-2"/> loads only at runtime, nothing in dev
- <ant-design-frown-filled class="text-red-400" /> no typings
  - no code completion
  - no safeguarding on build
- <ant-design-frown-filled class="text-red-400" /> get node by name is depth-first in scene graph, e.g. `modelScene.getObjectByName("rock001");`
- <ant-design-frown-filled class="text-red-400" /> models as public assets (no versioning, etc.)
- <ant-design-frown-filled class="text-red-400" /> always all models bundled bc the bundler does not know what are used

</v-clicks>
