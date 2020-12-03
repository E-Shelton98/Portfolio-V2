<template>
    <div>
        <div class="border border-gray-400 h-auto m-4 flex flex-col items-center">
            <div class="border border-gray-400 h-32 w-32 my-4 rounded-full">

            </div>
            <div class="h-24 mx-4 text-center">
                <h1 class="text-2xl">Hi! I'm Erik Shelton</h1>
                <h2 class="text-xl">I’m a software engineer who loves solving problems and bringing difficult concepts down to a tangible level.</h2>
            </div>
            <div class="mt-16 mx-1">
                <button class="btns" @click="onTechClick()">Technologies</button>
                <button class="btns" @click="onHobbiesClick()">Hobbies</button>
                <button class="btns" @click="onLifeClick()">Life</button>
            </div>
            <section class="p-2">Click a category to learn more about me!</section>
        </div>
        <div>
            <div class="border border-gray-400 h-auto m-4 p-2 text-center" v-if="Technologies">
                <h3>Technologies</h3>
                <div class="m-1 grid grid-rows-3 grid-cols-4">
                    <div class="tech row-start-1 col-start-1"></div>
                    <div class="tech row-start-1 col-start-2"></div>
                    <div class="tech row-start-1 col-start-3"></div>
                    <div class="tech row-start-1 col-start-4"></div>
                    <div class="tech row-start-2 col-start-1"></div>
                    <div class="tech row-start-2 col-start-2"></div>
                    <div class="tech row-start-2 col-start-3"></div>
                    <div class="tech row-start-2 col-start-4"></div>
                    <div class="tech row-start-3 col-start-1"></div>
                    <div class="tech row-start-3 col-start-2"></div>
                    <div class="tech row-start-3 col-start-3"></div>
                    <div class="tech row-start-3 col-start-4"></div>
                </div>
            </div>
            <div class="border border-gray-400 h-auto m-4 p-4 text-center" v-if="Hobbies">
                <h3>Hobbies</h3>
                <section>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Assumenda ipsam pariatur vero deserunt dolorem rem repellat. Ipsam corporis sit corrupti excepturi aut commodi. Necessitatibus repellat sapiente magni nobis ipsa consequatur? Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quisquam, repellat harum esse dolores perferendis minus quo tempore est illo dolor corrupti commodi eum fugit fugiat voluptates. Exercitationem molestiae libero accusamus. Lorem ipsum dolor, sit amet consectetur adipisicing elit. Est iure ipsum repellendus dolor enim, id mollitia consectetur excepturi, doloribus sequi voluptate ratione! Magnam nulla labore repellat, repellendus eaque veritatis eum.</section>
            </div>
            <div class="border border-gray-400 h-auto m-4 p-4 text-center" v-if="Life">
                <h3>Life</h3>
                <section>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Assumenda ipsam pariatur vero deserunt dolorem rem repellat. Ipsam corporis sit corrupti excepturi aut commodi. Necessitatibus repellat sapiente magni nobis ipsa consequatur? Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quisquam, repellat harum esse dolores perferendis minus quo tempore est illo dolor corrupti commodi eum fugit fugiat voluptates. Exercitationem molestiae libero accusamus. Lorem ipsum dolor, sit amet consectetur adipisicing elit. Est iure ipsum repellendus dolor enim, id mollitia consectetur excepturi, doloribus sequi voluptate ratione! Magnam nulla labore repellat, repellendus eaque veritatis eum.</section>
            </div>
        </div>
        <div class="my-8">
            <section class="text-center">Projects</section>
            <div class="h-24 my-4 flex justify-around items-center">
                <div class="projects" @click="stopRotatingProjects(1)"></div>
                <div class="projects" @click="stopRotatingProjects(2)"></div>
                <div class="projects" @click="stopRotatingProjects(3)"></div>
                <div class="projects" @click="restartRotatingProjects()">Restart</div>
            </div>
            <div class="bg-blue-400 border border-gray-400 h-auto m-4 text-center" v-if="DisplayRotatedProjects === 1">
                <h3>{{DisplayRotatedProjects}}</h3>
                <section>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Aliquid ipsa sint pariatur blanditiis officiis, iusto tempora debitis inventore suscipit ratione magnam saepe molestias consectetur eligendi voluptate sunt eveniet, temporibus perferendis? Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nemo impedit ut nihil at culpa, doloribus voluptas ipsum, in voluptatum voluptate sit ipsam repellat velit natus commodi ipsa? Possimus, repellat quae. Lorem ipsum, dolor sit amet consectetur adipisicing elit. Fugit voluptatum possimus eum nemo debitis dolore quibusdam doloremque assumenda odio nisi, quis provident? Ipsum tempora inventore distinctio quas perferendis quae odio.</section>
            </div>
            <div class="bg-green-400 border border-gray-400 h-auto m-4 text-center" v-if="DisplayRotatedProjects === 2">
                <h3>{{DisplayRotatedProjects}}</h3>
                <section>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Aliquid ipsa sint pariatur blanditiis officiis, iusto tempora debitis inventore suscipit ratione magnam saepe molestias consectetur eligendi voluptate sunt eveniet, temporibus perferendis? Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nemo impedit ut nihil at culpa, doloribus voluptas ipsum, in voluptatum voluptate sit ipsam repellat velit natus commodi ipsa? Possimus, repellat quae. Lorem ipsum, dolor sit amet consectetur adipisicing elit. Fugit voluptatum possimus eum nemo debitis dolore quibusdam doloremque assumenda odio nisi, quis provident? Ipsum tempora inventore distinctio quas perferendis quae odio.</section>
            </div>
            <div class="bg-red-400 border border-gray-400 h-auto m-4 text-center" v-if="DisplayRotatedProjects === 3">
                <h3>{{DisplayRotatedProjects}}</h3>
                <section>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Aliquid ipsa sint pariatur blanditiis officiis, iusto tempora debitis inventore suscipit ratione magnam saepe molestias consectetur eligendi voluptate sunt eveniet, temporibus perferendis? Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nemo impedit ut nihil at culpa, doloribus voluptas ipsum, in voluptatum voluptate sit ipsam repellat velit natus commodi ipsa? Possimus, repellat quae. Lorem ipsum, dolor sit amet consectetur adipisicing elit. Fugit voluptatum possimus eum nemo debitis dolore quibusdam doloremque assumenda odio nisi, quis provident? Ipsum tempora inventore distinctio quas perferendis quae odio.</section>
            </div>
            <div class="bg-purple-400 border border-gray-400 h-auto m-4 text-center" v-if="DisplayStaticProject === 1">
                <h3>{{DisplayStaticProject}}</h3>
                <section>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Aliquid ipsa sint pariatur blanditiis officiis, iusto tempora debitis inventore suscipit ratione magnam saepe molestias consectetur eligendi voluptate sunt eveniet, temporibus perferendis? Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nemo impedit ut nihil at culpa, doloribus voluptas ipsum, in voluptatum voluptate sit ipsam repellat velit natus commodi ipsa? Possimus, repellat quae. Lorem ipsum, dolor sit amet consectetur adipisicing elit. Fugit voluptatum possimus eum nemo debitis dolore quibusdam doloremque assumenda odio nisi, quis provident? Ipsum tempora inventore distinctio quas perferendis quae odio.</section>
            </div>
            <div class="bg-yellow-400 border border-gray-400 h-auto m-4 text-center" v-if="DisplayStaticProject === 2">
                <h3>{{DisplayStaticProject}}</h3>
                <section>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Aliquid ipsa sint pariatur blanditiis officiis, iusto tempora debitis inventore suscipit ratione magnam saepe molestias consectetur eligendi voluptate sunt eveniet, temporibus perferendis? Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nemo impedit ut nihil at culpa, doloribus voluptas ipsum, in voluptatum voluptate sit ipsam repellat velit natus commodi ipsa? Possimus, repellat quae. Lorem ipsum, dolor sit amet consectetur adipisicing elit. Fugit voluptatum possimus eum nemo debitis dolore quibusdam doloremque assumenda odio nisi, quis provident? Ipsum tempora inventore distinctio quas perferendis quae odio.</section>
            </div>
            <div class="bg-gray-400 border border-gray-400 h-auto m-4 text-center" v-if="DisplayStaticProject === 3">
                <h3>{{DisplayStaticProject}}</h3>
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
    name: 'AppHome',
    data () {
        return {
            Technologies: false,
            Hobbies: false,
            Life: false,
            DisplayRotatedProjects: 1,
            DisplayStaticProject: 0
        }
    },
    created () {
       setInterval(() => {
           if (this.DisplayRotatedProjects !== 3 && this.DisplayRotatedProjects !== 0){
               this.DisplayRotatedProjects += 1
           }
           else if (this.DisplayRotatedProjects !== 0) {
               this.DisplayRotatedProjects = 1
           }
       }, 5000)
    },
    methods: {
        onTechClick () {
            this.Hobbies = false
            this.Life = false
            this.Technologies = true
        },
        onHobbiesClick () {
            this.Technologies = false
            this.Life = false
            this.Hobbies = true
        },
        onLifeClick () {
            this.Technologies = false
            this.Hobbies = false
            this.Life = true
        },
        stopRotatingProjects (project) {
            this.DisplayRotatedProjects = 0
            this.DisplayStaticProject = project
        },
        restartRotatingProjects () {
            this.DisplayRotatedProjects = 1
            this.DisplayStaticProject = 0
        },
        visibilityChanged (isVisible, entry) {
            this.isVisible = isVisible
            console.log(entry)
        }
    }
}
</script>

<style>
    .btns {
        @apply border border-gray-400 h-8 w-28 m-1 rounded-md
    }
    .projects {
        @apply border border-gray-400 h-16 w-36 m-2
    }
    .tech {
        @apply border border-gray-400 h-16 w-16 m-2 justify-self-center
    }
</style>
