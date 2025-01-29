---
layout: cover
leftOrientation: center
---

<div class="relative">
    <h1 class="!text-5xl">Your Own Vite Plugin?<br>That's as easy as 1 2 3(D)</h1>
    <div class="absolute w-24 left-52 top-7" v-mark="{ at: 3, color: '#ab2657', type: 'underline' }"></div>
    <div class="absolute w-24 left-52 top-5" v-mark="{ at: 3, color: '#ab2657', type: 'underline' }"></div>
    <div class="absolute w-24 left-52 top-6" v-mark="{ at: 3, color: '#ab2657', type: 'underline' }"></div>
</div>

<div class="flex flex-col relative">
    <div>
        with <span class="color-[#26ab7a]">Thorsten Seyschab</span>
    </div>
    <ul class="absolute top-10" v-click="1">
        <li>Computer Scientist and Web Engineer</li>
        <li><mdi-school-outline class="baseColor mr-2" /> Master of Science in Computer Science</li>
        <li><mdi-worker-outline class="baseColor mr-2"/> Fullstack developer, Self-Employed</li>
        <!-- <li>based in Germany</li> -->
    </ul>
    <div
        class="absolute top-3 left-105 px-5 py-2 whitespace-nowrap flex flex-col gap-2"
        v-click="2"
        v-mark="{ at: 2, color: '#26ab7a', type: 'box' }"
    >
        <div class="flex">
            <mdi-web class="baseColor mt-0.5 mr-2" />
            <MyLink to="https://todde.tv/">todde.tv</MyLink>
        </div>
        <div class="flex">
            <mdi-github class="baseColor mt-0.5 mr-2" />
            <MyLink to="https://github.com/toddeTV">toddeTV</MyLink>
        </div>
        <div class="flex">
            <mdi-linkedin class="baseColor mt-0.5 mr-2" />
            <MyLink to="https://www.linkedin.com/in/toddetv/">toddeTV</MyLink>
        </div>
        <div class="flex">
            <simple-icons-x class="baseColor mt-0.5 mr-2" />
            <MyLink to="https://x.com/toddeTV">toddeTV</MyLink>
        </div>
        <div class="flex">
            <!-- TODO wrong discord URI? -->
            <mdi-discord class="baseColor mt-0.5 mr-2" />
            <MyLink to="https://discordapp.com/users/todde.tv/">todde.tv</MyLink>
        </div>
        <div class="flex">
            <simple-icons-bluesky class="baseColor mt-0.5 mr-2" />
            <MyLink to="https://bsky.app/profile/todde.tv">todde.tv</MyLink>
        </div>
    </div>
</div>
