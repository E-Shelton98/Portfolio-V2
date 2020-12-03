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
            <div class="border border-gray-400 h-auto m-4 text-center">
                <h3>Project Name</h3>
                <section>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Aliquid ipsa sint pariatur blanditiis officiis, iusto tempora debitis inventore suscipit ratione magnam saepe molestias consectetur eligendi voluptate sunt eveniet, temporibus perferendis? Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nemo impedit ut nihil at culpa, doloribus voluptas ipsum, in voluptatum voluptate sit ipsam repellat velit natus commodi ipsa? Possimus, repellat quae. Lorem ipsum, dolor sit amet consectetur adipisicing elit. Fugit voluptatum possimus eum nemo debitis dolore quibusdam doloremque assumenda odio nisi, quis provident? Ipsum tempora inventore distinctio quas perferendis quae odio.</section>
            </div>
        </div>
        <div class="border border-gray-400 m-4 grid grid-rows-7 grid-cols-2">
            <section class="border border-gray-400 m-2 row-start-1 row-end-7 col-start-2 col-end-3">Lorem ipsum dolor sit amet consectetur adipisicing elit. Nulla veniam aperiam iusto, ipsa repudiandae velit est cupiditate magni cum enim! Est quae nam eum, ad ipsum magnam mollitia magni quas. Lorem, ipsum dolor sit amet consectetur adipisicing elit. Molestias rerum debitis officia nihil commodi praesentium.</section>
            <label class="border border-gray-400 h-12 w-auto row-start-1 col-start-1 m-4"></label>
            <input type="text" class="border border-gray-400 h-12 w-auto m-4 row-start-2 col-start-1">
            <label class="border border-gray-400 h-12 w-auto row-start-3 col-start-1 m-4"></label>
            <input type="text" class="border border-gray-400 h-12 w-auto m-4 row-start-4 col-start-1">
            <label class="border border-gray-400 h-12 w-auto row-start-5 col-start-1 m-4"></label>
            <input type="text" class="border border-gray-400 h-12 w-auto m-4 row-start-6 col-start-1">
            <submit class="border border-gray-400 h-12 w-auto m-2 row-start-7 col-start-1 col-span-2"></submit>
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