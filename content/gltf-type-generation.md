---
layout: basic
---

# glTF type generation

<v-clicks :depth="2">

- <ant-design-frown-filled class="text-red-400" /> `three.js` is for runtime, especially the loaders (only in browser, not in node runtime)
  - <ant-design-smile-filled class="text-green-400" /> solution: patch and implement it
- <ant-design-frown-filled class="text-red-400" /> problem with patch: we need two GLTFLoaders & a patch would patch both:<br>
  1. patched for plugin, version fixed, bundled<br>
  2. original for user, version free, not bundled<br>
  - <ant-design-smile-filled class="text-green-400" /> solution: use `three-stdlib` (extraction of the `three.js` examples directory)

</v-clicks>
