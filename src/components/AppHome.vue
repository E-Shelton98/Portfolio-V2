<template>
    <div class="bg-gradient-to-b from-green-200 via-indigo-400 to-purple-400 p-2">
        <div class="border-2 border-purple-900 border-opacity-25 h-auto m-4 rounded-lg flex flex-col items-center">
            <div class="bg-white border border-green-400 h-32 w-32 my-4 rounded-full flex justify-center items-center lg:h-40 lg:w-40">
                <img src="https://res.cloudinary.com/dm5cjaisp/image/upload/v1600230047/IMG_0272_bxi0xu.jpg" class="overflow-hidden h-28 w-28 rounded-full lg:h-36 lg:w-36">
            </div>
            <div class="h-auto text-center">
                <h1 class="text-2xl">Hi! I'm Erik Shelton</h1>
                <h2 class="text-xl">I’m a software engineer who loves solving problems and bringing difficult concepts down to a tangible level.</h2>
            </div>
            <div class="m-2 flex flex-col md:flex-row">
                <button class="bg-green-500 border border-green-500 h-8 w-28 m-1 rounded-md focus:outline-none focus:ring-2 focus:ring-purple-900 focus:ring-opacity-50 focus:bg-green-300" @click="onTechClick()">Technologies</button>
                <button class="bg-green-500 border border-green-500 h-8 w-28 m-1 rounded-md focus:outline-none focus:ring-2 focus:ring-purple-900 focus:ring-opacity-50 focus:bg-green-300" @click="onHobbiesClick()">Hobbies</button>
                <button class="bg-green-500 border border-green-500 h-8 w-28 m-1 rounded-md focus:outline-none focus:ring-2 focus:ring-purple-900 focus:ring-opacity-50 focus:bg-green-300" @click="onLifeClick()">Life</button>
            </div>
            <section class="p-2">Click a category to learn more about me!</section>
        </div>
        <div>
            <transition name="fade">
                <div class="border border-purple-900 border-opacity-50 rounded-lg h-auto m-4 p-2" v-if="Technologies">
                    <h3 class="text-center text-2xl underline">Technologies</h3>
                    <div class="m-1 grid grid-rows-2 grid-cols-4">
                        <div class="bg-white border-2 border-purple-900 rounded-2xl h-16 w-16 m-2 justify-self-center row-start-1 col-start-1">
                            <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/9/95/Vue.js_Logo_2.svg/1184px-Vue.js_Logo_2.svg.png' alt="vue.js logo" class="pt-4 p-2">
                            </div>
                        <div class="bg-white border-2 border-purple-900 rounded-2xl h-16 w-16 m-2 justify-self-center row-start-1 col-start-2">
                            <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/a/a7/React-icon.svg/320px-React-icon.svg.png' alt="React.js logo" class="pt-2"></div>
                        <div class="bg-white border-2 border-purple-900 rounded-2xl h-16 w-16 m-2 justify-self-center row-start-1 col-start-3">
                            <img src="https://pbs.twimg.com/profile_images/1278691829135876097/I4HKOLJw_400x400.png" alt="tailwindCSS logo" class="h-14 pl-2 pt-2">
                        </div>
                        <div class="bg-white border-2 border-purple-900 rounded-2xl h-16 w-16 m-2 justify-self-center row-start-1 col-start-4">
                            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/73/Ruby_logo.svg/1024px-Ruby_logo.svg.png" alt="ruby logo" class="h-12 pt-2 pl-2">
                        </div>
                        <div class="bg-white border-2 border-purple-900 rounded-2xl h-16 w-16 m-2 justify-self-center row-start-2 col-start-1">
                            <img src="https://miro.medium.com/max/800/1*eRErB-NQYgwF52eUUK_kkQ.png" alt="rails logo" class="p-2">
                        </div>
                        <div class="bg-white border-2 border-purple-900 rounded-2xl h-16 w-16 m-2 justify-self-center row-start-2 col-start-2">
                            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/c3/Python-logo-notext.svg/768px-Python-logo-notext.svg.png" alt="python logo" class="p-2">
                        </div>
                        <div class="bg-white border-2 border-purple-900 rounded-2xl h-16 w-16 m-2 justify-self-center row-start-2 col-start-3">
                            <img src="https://raw.githubusercontent.com/isocpp/logos/master/cpp_logo.png" alt="C++ logo" class="p-3">
                        </div>
                        <div class="bg-white border-2 border-purple-900 rounded-2xl h-16 w-16 m-2 justify-self-center row-start-2 col-start-4">
                            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/29/Postgresql_elephant.svg/1200px-Postgresql_elephant.svg.png" alt="postgresql logo" class="p-2">
                        </div>
                    </div>
                </div>
            </transition>
            <transition name="fade">
                <div class="border border-purple-900 border-opacity-50 rounded-lg h-auto m-4 p-4 text-justify" v-if="Hobbies">
                    <h3 class="text-center text-xl">Hobbies</h3>
                    <section>Beyond just programming, I love solving problems and puzzles. I also have a passion for learning and teaching others, and greatly enjoy taking part in helping people learn new complex things. I've recently started looking into blogging, making a youtube series, and possibly some tutorials over Vue that I have recently found a passion in. Outside of the world of programming, I am passionate about all things tech, greatly enjoy cars and all things fast, love working on mechanical things such as R/C racing, and I play a healthy dose of video games when time around my many projects allow me. Other than that I would say my greatest hobby is simply spending time with my family and trying to enjoy the life that I've built or that has been handed to me.</section>
                </div>
            </transition>
            <transition name="fade">
                <div class="border border-purple-900 border-opacity-50 rounded-lg h-auto m-4 p-4 text-justify" v-if="Life">
                    <h3 class="text-center text-xl">Life</h3>
                    <section>Born and raised in Ohio, I come from the small town life. I'm used to living in communities where everyone knows everybody, but would be very happy in a large city with a few close friends as well. I have a beautiful wife that I am blessed to call my own and currently we live close to our hometown but hope to some day move. I've been to quite a few different places in the country and have found that I love to travel when I can. I found from a young age that I was strong at problem solving, and knew from then that I would someday have a job that revolved around that talent. After working in tech support in high school I transitioned into a few various factory jobs while working on building my passion for programming.</section>
                </div>
            </transition>
        </div>
        <div class="my-8">
            <h3 class="text-center text-2xl underline">Projects</h3>
            <section class="text-center italic">Click a project number to stop the rotation</section>
            <div class="h-auto my-4 flex justify-around items-center">
                <div class="bg-green-500 border border-green-400 rounded-md h-12 w-12 m-2 flex justify-center items-center lg:h-16 lg:w-16" @click="stopRotatingProjects(1)">
                    <section>P1</section>
                </div>
                <div class="bg-green-500 border border-green-400 rounded-md h-12 w-12 m-2 flex justify-center items-center lg:h-16 lg:w-16" @click="stopRotatingProjects(2)">
                    <section>P2</section>
                </div>
                <div class="bg-green-500 border border-green-400 rounded-md h-12 w-12 m-2 flex justify-center items-center lg:h-16 lg:w-16" @click="stopRotatingProjects(3)">
                    <section>P3</section>
                </div>
            </div>
            <div class="border border-purple-900 rounded-md h-auto m-4 p-2 text-justify md:flex md:flex-col lg:grid" v-if="DisplayRotatedProjects === 1 || DisplayStaticProject === 1">
                <h3 class="text-center text-2xl lg:row-start-1 lg:col-start-1 lg:col-span-2">MTG-Deck-Maker</h3>
                <img src="https://res.cloudinary.com/dm5cjaisp/image/upload/v1607389608/Screen_Shot_2020-12-07_at_8.05.42_PM_sa8mzg.png" class="p-2 md:h-3/4 md:w-3/4 md:self-center lg:h-60 lg:w-96 lg:row-start-2 lg:col-start-1">
                <div class="md:relative h-full p-2 lg:row-start-2 lg:col-start-2"><section class="pb-8">A simple deck maker created using React for Magic: The Gathering, using Chart.js to display various graphs that give further insight to your currently created deck such as mana values, card amounts, card types, and mana color spread.
                </section>
                <a href="https://e-shelton-mtgdeckmaker.netlify.app" class=" md:absolute md:bottom-0 md:left-0">Click to View</a>
                <div @click="restartRotatingProjects()" class="md:absolute md:bottom-0 md:right-0 text-left">Click to Restart Rotating Projects</div></div>
            </div>
            <div class="border border-purple-900 rounded-md h-auto m-4 p-2 text-justify md:flex md:flex-col lg:grid" v-if="DisplayRotatedProjects === 2 || DisplayStaticProject === 2">
                <h4 class="text-center text-2xl lg:row-start-1 lg:col-start-1 lg:col-span-2">Sticky Task</h4>
                <img src="https://res.cloudinary.com/dm5cjaisp/image/upload/v1607391604/Screen_Shot_2020-12-07_at_8.39.38_PM_snavw0.png" class="p-2 md:h-3/4 md:w-3/4 md:self-center lg:h-60 lg:w-full lg:row-start-2 lg:col-start-1">
                <div class="md:relative h-full p-2 lg:row-start-2 lg:col-start-2"><section class="pb-8">A group project using React, with a rails backend; the premise is that you can create tasks likewise to "sticky notes" to be able to assign to "taskers" whether they be workers, students, or children. My work was primarily in the frontend of the project, though I did help with bug fixes from time to time on the backend of the project.</section>
                <a href="https://sticky-task.netlify.app" class=" md:absolute md:bottom-0 md:left-0">Click to View</a>
                <div class="md:absolute md:bottom-0 md:right-0 text-left" @click="restartRotatingProjects()">Click to Restart Rotating Projects</div></div>
            </div>
            <div class="border border-purple-900 rounded-md h-auto m-4 p-2 text-justify md:flex md:flex-col lg:grid" v-if="DisplayRotatedProjects === 3 || DisplayStaticProject === 3">
                <h3 class="text-center text-2xl lg:row-start-1 lg:col-start-1 lg:col-span-2">Random Card</h3>
                <img src="https://res.cloudinary.com/dm5cjaisp/image/upload/v1600118869/Screen_Shot_2020-09-14_at_5.27.29_PM_gqngnd.png" class="p-2 md:h-3/4 md:w-3/4 md:self-center lg:h-60 lg:w-96 lg:row-start-2 lg:col-start-1">
                <div class="md:relative h-full p-2 lg:row-start-2 lg:col-start-2"><section class="pb-8">A Javascript program that uses a deck of cards and will deal a random card each time you click the "add a card" button.</section>
                <a href="https://pages.git.generalassemb.ly/E-Shelton98/W02D04-HW/random_imager/" class=" md:absolute md:bottom-0 md:left-0">Click to View</a>
                <div class="md:absolute md:bottom-0 md:right-0 text-left" @click="restartRotatingProjects()">Click to Restart Rotating Projects</div></div>
            </div>
        </div>
        <div class="border border-gray-900 rounded-lg m-4">
            <section class="m-2 text-center text-xl underline">Lets Work Together</section>
            <section class="m-2 text-center">Email: codewerik@gmail.com</section>
            <section class="m-2 text-center">View my <a href="https://github.com/E-Shelton98" class="underline">GitHub</a></section>
            <section class="m-2 text-center">Connect on <a href="https://www.linkedin.com/in/erik-shelton-07a932192/" class="underline">LinkedIn</a></section>
            
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
            this.Technologies = !this.Technologies
        },
        onHobbiesClick () {
            this.Technologies = false
            this.Life = false
            this.Hobbies = !this.Hobbies
        },
        onLifeClick () {
            this.Technologies = false
            this.Hobbies = false
            this.Life = !this.Life
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

<style scoped>
.fade-enter-active{
    transition: opacity 1s ease;
}

.fade-enter-from
{
    opacity: 0;
}
</style>
