---
layout: basic
---

# Game, Code & Licenses

<div class="absolute right-15 top-15 p-1 pr-2" v-mark="{ at: 0, color: '#26ab7a', type: 'box' }">
    <mdi-heart class="text-red-400 animate-pulse mx-2" /> Andreas Fehn <mdi-github class="baseColor mx-2" /> <MyLink to="https://github.com/fehnomenal">fehnomenal</MyLink>
</div>

<div class="flex flex-row gap-8 mt-8">
    <div
        class="p-4 flex flex-col items-center"
        v-mark="{ at: 0, color: '#26ab7a', type: 'box' }"
    >
        <QRCode value="https://zlig.net/" :size="128" class="mb-6" />
        <div class="flex flex-col gap-2">
            <div class="whitespace-nowrap">
                Game Online:
            </div>
            <div class="whitespace-nowrap">
                <mdi-web class="baseColor mx-2" />
                <MyLink to="https://zlig.net/">https://zlig.net/</MyLink>
            </div>
        </div>
    </div>
    <div
        class="p-4 flex flex-col items-center"
        v-mark="{ at: 0, color: '#26ab7a', type: 'box' }"
    >
        <QRCode value="https://github.com/toddeTV/zlig" :size="128" class="mb-6" />
        <div class="flex flex-col gap-2">
            <div class="whitespace-nowrap">
                Game Source-Code:
            </div>
            <div class="whitespace-nowrap">
                <mdi-github class="baseColor mx-2" />
                <MyLink to="https://github.com/toddeTV/zlig">https://github.com/toddeTV/zlig</MyLink>
            </div>
        </div>
    </div>
    <div
        class="p-4 flex flex-col items-center"
        v-mark="{ at: 0, color: '#26ab7a', type: 'box' }"
    >
        <QRCode value="https://github.com/toddeTV/talk_2025-01-29_vue-js-nation-conference" :size="128" class="mb-6" />
        <div class="flex flex-col gap-2">
            <div class="whitespace-nowrap">
                Presentation slides Source-Code:
            </div>
            <div class="w-full">
                <mdi-github class="baseColor mx-2" />
                <MyLink to="https://github.com/toddeTV/talk_2025-01-29_vue-js-nation-conference">https://github.com/toddeTV/talk_2025-01-29_vue-js-nation-conference</MyLink>
            </div>
        </div>
    </div>
</div>

<div class="mt-8 p-2" v-mark="{ at: 0, color: '#26ab7a', type: 'box' }">
    <h2 class="!mb-2 !mt-0">Licenses</h2>
    <div class="text-xs">
        For detailed information regarding the materials used in this presentation - including 3D models, images, dependencies, icon packs, etc. - and their respective licenses and copyrights, please refer to the <code>README.md</code> file in the publicly available source code of these presentation slides, see above.
    </div>
</div>
