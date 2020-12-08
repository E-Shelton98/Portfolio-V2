<template>
    <div class="bg-gradient-to-b from-green-200 via-indigo-400 to-purple-700 p-2">
        <div class="border-2 border-purple-900 border-opacity-25 h-auto m-4 rounded-lg flex flex-col items-center">
            <div class="border border-green-400 h-32 w-32 my-4 rounded-full">

            </div>
            <div class="h-24 mx-4 text-center">
                <h1 class="text-2xl">Hi! I'm Erik Shelton</h1>
                <h2 class="text-xl">I’m a software engineer who loves solving problems and bringing difficult concepts down to a tangible level.</h2>
            </div>
            <div class="mt-16 mx-1">
                <button class="bg-green-500 border border-green-500 h-8 w-28 m-1 rounded-md focus:outline-none focus:ring-2 focus:ring-purple-900 focus:ring-opacity-50 focus:bg-green-300" @click="onTechClick()">Technologies</button>
                <button class="bg-green-500 border border-green-500 h-8 w-28 m-1 rounded-md focus:outline-none focus:ring-2 focus:ring-purple-900 focus:ring-opacity-50 focus:bg-green-300" @click="onHobbiesClick()">Hobbies</button>
                <button class="bg-green-500 border border-green-500 h-8 w-28 m-1 rounded-md focus:outline-none focus:ring-2 focus:ring-purple-900 focus:ring-opacity-50 focus:bg-green-300" @click="onLifeClick()">Life</button>
            </div>
            <section class="p-2">Click a category to learn more about me!</section>
        </div>
        <div>
            <div class="border border-purple-900 border-opacity-50 rounded-lg h-auto m-4 p-2" v-if="Technologies">
                <h3 class="text-center">Technologies</h3>
                <div class="m-1 grid grid-rows-2 grid-cols-4">
                    <div class="bg-white border border-purple-900 rounded-2xl h-16 w-16 m-2 justify-self-center row-start-1 col-start-1">
                        <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/9/95/Vue.js_Logo_2.svg/1184px-Vue.js_Logo_2.svg.png' alt="vue.js logo" class="pt-4 p-2"></div>
                    <div class="bg-white border border-purple-900 rounded-2xl h-16 w-16 m-2 justify-self-center row-start-1 col-start-2">
                        <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/a/a7/React-icon.svg/320px-React-icon.svg.png' alt="React.js logo" class="pt-2"></div>
                    <div class="bg-white border border-purple-900 rounded-2xl h-16 w-16 m-2 justify-self-center row-start-1 col-start-3">
                        <img src="https://pbs.twimg.com/profile_images/1278691829135876097/I4HKOLJw_400x400.png" alt="tailwindCSS logo" class="h-14 pl-2 pt-2">
                    </div>
                    <div class="bg-white border border-purple-900 rounded-2xl h-16 w-16 m-2 justify-self-center row-start-1 col-start-4">
                        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/73/Ruby_logo.svg/1024px-Ruby_logo.svg.png" alt="ruby logo" class="h-12 pt-2 pl-2">
                    </div>
                    <div class="bg-white border border-purple-900 rounded-2xl h-16 w-16 m-2 justify-self-center row-start-2 col-start-1">
                        <img src="https://miro.medium.com/max/800/1*eRErB-NQYgwF52eUUK_kkQ.png" alt="rails logo" class="p-2">
                    </div>
                    <div class="bg-white border border-purple-900 rounded-2xl h-16 w-16 m-2 justify-self-center row-start-2 col-start-2">
                        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/c3/Python-logo-notext.svg/768px-Python-logo-notext.svg.png" alt="python logo" class="p-2">
                    </div>
                    <div class="bg-white border border-purple-900 rounded-2xl h-16 w-16 m-2 justify-self-center row-start-2 col-start-3">
                        <img src="https://raw.githubusercontent.com/isocpp/logos/master/cpp_logo.png" alt="C++ logo" class="p-3">
                    </div>
                    <div class="bg-white border border-purple-900 rounded-2xl h-16 w-16 m-2 justify-self-center row-start-2 col-start-4">
                        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/29/Postgresql_elephant.svg/1200px-Postgresql_elephant.svg.png" alt="postgresql logo" class="p-2">
                    </div>
                </div>
            </div>
            <div class="border border-purple-900 border-opacity-50 rounded-lg h-auto m-4 p-4 text-center" v-if="Hobbies">
                <h3>Hobbies</h3>
                <section>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Assumenda ipsam pariatur vero deserunt dolorem rem repellat. Ipsam corporis sit corrupti excepturi aut commodi. Necessitatibus repellat sapiente magni nobis ipsa consequatur? Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quisquam, repellat harum esse dolores perferendis minus quo tempore est illo dolor corrupti commodi eum fugit fugiat voluptates. Exercitationem molestiae libero accusamus. Lorem ipsum dolor, sit amet consectetur adipisicing elit. Est iure ipsum repellendus dolor enim, id mollitia consectetur excepturi, doloribus sequi voluptate ratione! Magnam nulla labore repellat, repellendus eaque veritatis eum.</section>
            </div>
            <div class="border border-purple-900 border-opacity-50 rounded-lg h-auto m-4 p-4 text-center" v-if="Life">
                <h3>Life</h3>
                <section>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Assumenda ipsam pariatur vero deserunt dolorem rem repellat. Ipsam corporis sit corrupti excepturi aut commodi. Necessitatibus repellat sapiente magni nobis ipsa consequatur? Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quisquam, repellat harum esse dolores perferendis minus quo tempore est illo dolor corrupti commodi eum fugit fugiat voluptates. Exercitationem molestiae libero accusamus. Lorem ipsum dolor, sit amet consectetur adipisicing elit. Est iure ipsum repellendus dolor enim, id mollitia consectetur excepturi, doloribus sequi voluptate ratione! Magnam nulla labore repellat, repellendus eaque veritatis eum.</section>
            </div>
        </div>
        <div class="my-8">
            <section class="text-center">Projects</section>
            <div class="h-24 my-4 flex justify-around items-center">
                <div class="border border-gray-400 h-16 w-36 m-2" @click="stopRotatingProjects(1)"></div>
                <div class="border border-gray-400 h-16 w-36 m-2" @click="stopRotatingProjects(2)"></div>
                <div class="border border-gray-400 h-16 w-36 m-2" @click="stopRotatingProjects(3)"></div>
                <div class="border border-gray-400 h-16 w-36 m-2" @click="restartRotatingProjects()">Restart</div>
            </div>
            <div class="bg-blue-400 border border-gray-400 h-auto m-4 text-center" v-if="DisplayRotatedProjects === 1 || DisplayStaticProject === 1">
                <h3>{{DisplayRotatedProjects}}</h3>
                <section>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Aliquid ipsa sint pariatur blanditiis officiis, iusto tempora debitis inventore suscipit ratione magnam saepe molestias consectetur eligendi voluptate sunt eveniet, temporibus perferendis? Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nemo impedit ut nihil at culpa, doloribus voluptas ipsum, in voluptatum voluptate sit ipsam repellat velit natus commodi ipsa? Possimus, repellat quae. Lorem ipsum, dolor sit amet consectetur adipisicing elit. Fugit voluptatum possimus eum nemo debitis dolore quibusdam doloremque assumenda odio nisi, quis provident? Ipsum tempora inventore distinctio quas perferendis quae odio.</section>
            </div>
            <div class="bg-green-400 border border-gray-400 h-auto m-4 text-center" v-if="DisplayRotatedProjects === 2 || DisplayStaticProject === 2">
                <h3>{{DisplayRotatedProjects}}</h3>
                <section>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Aliquid ipsa sint pariatur blanditiis officiis, iusto tempora debitis inventore suscipit ratione magnam saepe molestias consectetur eligendi voluptate sunt eveniet, temporibus perferendis? Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nemo impedit ut nihil at culpa, doloribus voluptas ipsum, in voluptatum voluptate sit ipsam repellat velit natus commodi ipsa? Possimus, repellat quae. Lorem ipsum, dolor sit amet consectetur adipisicing elit. Fugit voluptatum possimus eum nemo debitis dolore quibusdam doloremque assumenda odio nisi, quis provident? Ipsum tempora inventore distinctio quas perferendis quae odio.</section>
            </div>
            <div class="bg-red-400 border border-gray-400 h-auto m-4 text-center" v-if="DisplayRotatedProjects === 3 || DisplayStaticProject === 3">
                <h3>{{DisplayRotatedProjects}}</h3>
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
            SheetAsJSON: 'https://spreadsheets.google.com/feeds/list/1K-_6L0kigNrVAYvP_9uw2-4E-tnn1VQ0RTahYK_4Rd0/od6/public/values?alt=json',
            Technologies: false,
            Hobbies: false,
            Life: false,
            DisplayRotatedProjects: 1,
            DisplayStaticProject: 0,
            projectList: [],
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
    }
}
</script>

<style>

</style>
