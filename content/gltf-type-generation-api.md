---
layout: basic
---

# glTF type generation - API Design

Decision: What do we want to focus on in the final user app?

<v-clicks>

- **usability:** prioritize by usage e.g. `IslandScene.island.beach.rock001`
  - <mdi-code class="text-gray-400" /> Implement by packing the model in one (potentially very large) object
  - <ant-design-smile-filled class="text-green-400" /> good usability bc user can use the scene graph that mirrors the glTF structure to navigate
  - <ant-design-frown-filled class="text-red-400" /> larger bundle size due to the one (potentially very large) object
- **bundle size:** prioritize by usage e.g. `getRock001(getBeach(getIsland(getIslandScene(model))))`
  - <mdi-code class="text-gray-400" /> Implement by e.g. `function getSomething(parent) { return parent.children[xxx]; }`
  - <ant-design-smile-filled class="text-green-400" /> unused functions could get tree-shaken
  - <ant-design-frown-filled class="text-red-400" /> not very user friendly
- **combination**: crawl the user code & generate only used paths as direct pointer
  - <ant-design-frown-filled class="text-red-400" /> crawling user applications? Really?

</v-clicks>
