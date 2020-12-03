<template>
    <div>
        <div class="border border-gray-400 h-96 m-4 flex flex-col items-center">
            <div class="border border-gray-400 h-32 w-32 my-4 rounded-full">

            </div>
            <div class="h-24 mx-4">
                <section>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Magnam consectetur hic rerum atque ratione debitis, nulla mollitia at quo optio a ducimus dignissimos saepe, laborum ea. Enim ratione nulla vero.</section>
            </div>
            <div class="mt-16 mx-1">
                <button class="btns"></button>
                <button class="btns"></button>
                <button class="btns"></button>
                <button class="btns"></button>
            </div>
        </div>
        <div class="border border-gray-400 h-auto m-8">
            <div class="h-auto m-4">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Assumenda ipsam pariatur vero deserunt dolorem rem repellat. Ipsam corporis sit corrupti excepturi aut commodi. Necessitatibus repellat sapiente magni nobis ipsa consequatur? Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quisquam, repellat harum esse dolores perferendis minus quo tempore est illo dolor corrupti commodi eum fugit fugiat voluptates. Exercitationem molestiae libero accusamus. Lorem ipsum dolor, sit amet consectetur adipisicing elit. Est iure ipsum repellendus dolor enim, id mollitia consectetur excepturi, doloribus sequi voluptate ratione! Magnam nulla labore repellat, repellendus eaque veritatis eum.</div>
        </div>
        <div class="border-2 border-red-400 my-4">
            <section class="text-center">Projects</section>
            <div class="h-24 my-4 flex justify-around items-center">
                <div class="projects"></div>
                <div class="projects"></div>
                <div class="projects"></div>
            </div>
            <div class="border border-gray-400 h-auto m-4">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quo nulla dolor, esse blanditiis unde facere, inventore eveniet quisquam asperiores iure veritatis voluptatibus illo, sapiente ipsa eos dolore incidunt consequuntur vero! Lorem ipsum dolor sit amet consectetur adipisicing elit. Iure placeat fugiat velit, voluptatem esse sint veritatis vel nostrum eos, nihil ducimus quaerat atque natus. Facere iure itaque molestias reiciendis natus. Lorem, ipsum dolor sit amet consectetur adipisicing elit. Incidunt eaque harum id molestias voluptatum enim necessitatibus nulla, optio ut dolores facilis! Illo aspernatur dolore animi ea cumque nihil deserunt eum.</div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'AppHome'
}
</script>

<style>
    .btns {
        @apply border border-gray-400 h-8 w-24 m-1 rounded-md
    }
    .projects {
        @apply border border-gray-400 h-16 w-36 m-2
    }
</style>