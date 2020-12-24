<template>
    <div class="flex flex-col lg:w-auto mt-2 max-w-screen-xl">
        <div class="bg-gradient-to-br from-green-300 to-blue-300 h-auto rounded-lg grid items-center ">
            <h1 class="text-2xl text-center pt-2 md:pt-10 row-start-1 col-start-2 self-start justify-self-start">Hello! I'm Erik Shelton</h1>
            <div class="h-32 w-32 md:h-48 md:w-48 my-4 rounded-full flex justify-center items-center overflow-hidden row-start-1 col-start-1 justify-self-center">
                <img src="https://res.cloudinary.com/dm5cjaisp/image/upload/v1600230047/IMG_0272_bxi0xu.jpg" class="h-auto w-full rounded-full object-cover">
            </div>
            <div class="h-auto w-72 text-center row-start-1 col-start-2 self-center justify-self-start">
                <h2 class="text-lg text-left pt-8 leading-normal">I’m a software engineer who loves solving problems and bringing difficult concepts down to a tangible level.</h2>
            </div>
        </div>
        <div class="mt-4 flex flex-col items-center">
            <div class="bg-gradient-to-tl from-green-300 via-purple-200 to-blue-300 p-2 flex flex-col rounded-lg h-auto w-full max-w-screen-xl">
                <h2 class="text-2xl underline text-center pb-2">About Me</h2>
                <div class="mb-2 flex justify-center">
                    <button class="border-2 border-black h-8 w-28 m-1 lg:mx-4 rounded-md ring-2 ring-gray-400 ring-inset focus:outline-none focus:bg-green-300" @click="onTechClick()">Technologies</button>
                    <button class="border-2 border-black h-8 w-28 m-1 lg:mx-4 rounded-md ring-2 ring-gray-400 ring-inset focus:outline-none focus:bg-green-300" @click="onHobbiesClick()">Hobbies</button>
                    <button class="border-2 border-black h-8 w-28 m-1 lg:mx-4 rounded-md ring-2 ring-gray-400 ring-inset focus:outline-none focus:bg-green-300" @click="onLifeClick()">Life</button>
                </div>
                <transition name="fade">
                <div class="bg-blue-300 rounded-lg h-auto pt-2 mb-2" v-if="Technologies">
                    <h3 class="text-center text-2xl underline">Technologies</h3>
                    <div class="m-1 grid grid-rows-2 grid-cols-4">
                        <div class="bg-white border-2 border-purple-900 rounded-2xl h-16 w-16 m-2 justify-self-center row-start-1 col-start-1 flex justify-center items-center">
                            <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/9/95/Vue.js_Logo_2.svg/1184px-Vue.js_Logo_2.svg.png' alt="vue.js logo" class="p-2">
                            </div>
                        <div class="bg-white border-2 border-purple-900 rounded-2xl h-16 w-16 m-2 justify-self-center row-start-1 col-start-2 flex justify-center items-center">
                            <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/a/a7/React-icon.svg/320px-React-icon.svg.png' alt="React.js logo"></div>
                        <div class="bg-white border-2 border-purple-900 rounded-2xl h-16 w-16 m-2 justify-self-center row-start-1 col-start-3 flex justify-center items-center">
                            <img src="https://pbs.twimg.com/profile_images/1278691829135876097/I4HKOLJw_400x400.png" alt="tailwindCSS logo" class="p-1">
                        </div>
                        <div class="bg-white border-2 border-purple-900 rounded-2xl h-16 w-16 m-2 justify-self-center row-start-1 col-start-4 flex justify-center items-center">
                            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/73/Ruby_logo.svg/1024px-Ruby_logo.svg.png" alt="ruby logo" class="p-2">
                        </div>
                        <div class="bg-white border-2 border-purple-900 rounded-2xl h-16 w-16 m-2 justify-self-center row-start-2 col-start-1 flex justify-center items-center">
                            <img src="https://miro.medium.com/max/800/1*eRErB-NQYgwF52eUUK_kkQ.png" alt="rails logo" class="p-1">
                        </div>
                        <div class="bg-white border-2 border-purple-900 rounded-2xl h-16 w-16 m-2 justify-self-center row-start-2 col-start-2 flex justify-center items-center">
                            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/c3/Python-logo-notext.svg/768px-Python-logo-notext.svg.png" alt="python logo" class="p-1">
                        </div>
                        <div class="bg-white border-2 border-purple-900 rounded-2xl h-16 w-16 m-2 justify-self-center row-start-2 col-start-3 flex justify-center items-center">
                            <img src="https://raw.githubusercontent.com/isocpp/logos/master/cpp_logo.png" alt="C++ logo" class="p-2">
                        </div>
                        <div class="bg-white border-2 border-purple-900 rounded-2xl h-16 w-16 m-2 justify-self-center row-start-2 col-start-4 flex justify-center items-center">
                            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/29/Postgresql_elephant.svg/1200px-Postgresql_elephant.svg.png" alt="postgresql logo" class="p-1">
                        </div>
                    </div>
                </div>
                </transition>
                <transition name="fade">
                <div class="bg-purple-200 rounded-lg h-auto pt-2 mb-2" v-if="Hobbies">
                    <h3 class="text-center text-xl">Hobbies</h3>
                    <section class="p-2">Beyond just programming, I love solving problems and puzzles. I also have a passion for learning and teaching others, and greatly enjoy taking part in helping people learn new complex things. I've recently started looking into blogging, making a youtube series, and possibly some tutorials over Vue that I have recently found a passion in. Outside of the world of programming, I am passionate about all things tech, greatly enjoy cars and all things fast, love working on mechanical things such as R/C racing, and I play a healthy dose of video games when time around my many projects allow me.</section>
                </div>
                </transition>
                <transition name="fade">
                <div class="bg-green-300 rounded-lg h-auto pt-2 mb-2" v-if="Life">
                    <h3 class="text-center text-xl">Life</h3>
                    <section class="p-2">Born and raised in Ohio, I come from the small town life. I'm used to living in communities where everyone knows everybody, but would be very happy in a large city with a few close friends as well. I have a beautiful wife that I am blessed to call my own and currently we live close to our hometown but hope to some day move. I've been to quite a few different places in the country and have found that I love to travel when I can. I found from a young age that I was strong at problem solving, and knew from then that I would someday have a job that revolved around that talent.</section>
                </div>
                </transition>
            </div>
                
            <div class="bg-gradient-to-bl from-green-300 via-purple-200 to-blue-300 my-4 rounded-lg max-w-screen-xl">
                <h3 class="text-center text-2xl underline pt-2">Projects</h3>
                <div class="h-auto my-4 flex justify-around items-center">
                    <div class="bg-green-500 border border-green-400 rounded-md h-12 w-20 m-2 flex justify-center items-center" @click="stopRotatingProjects(1)">
                        <section>Project 1</section>
                    </div>
                    <div class="bg-green-500 border border-green-400 rounded-md h-12 w-20 m-2 flex justify-center items-center" @click="stopRotatingProjects(2)">
                        <section>Project 2</section>
                    </div>
                    <div class="bg-green-500 border border-green-400 rounded-md h-12 w-20 m-2 flex justify-center items-center" @click="stopRotatingProjects(3)">
                        <section>Project 3</section>
                    </div>
                </div>
                <div class="rounded-md h-auto md:h-96 m-4 p-2 text-justify md:grid" v-if="DisplayRotatedProjects === 1 || DisplayStaticProject === 1">
                    <h3 class="text-center text-2xl md:row-start-1 md:col-start-3">MTG-Deck-Maker</h3>
                    <div class="md:row-start-1 md:row-end-3 md:col-start-1 md:col-end-3 h-48 md:h-full w-auto max-w-2xl">
                        <img src="https://res.cloudinary.com/dm5cjaisp/image/upload/v1607389608/Screen_Shot_2020-12-07_at_8.05.42_PM_sa8mzg.png" class="pr-2 h-full w-full object-contain">
                    </div>
                    <div class="md:relative h-72 md:h-full p-2 md:row-start-2 md:col-start-3">
                        <section class="pb-8 pt-4">A simple deck maker created using React for Magic: The Gathering, using Chart.js to display various graphs that give further insight to your currently created deck such as mana values, card amounts, card types, and mana color spread.
                        </section>
                        <a href="https://e-shelton-mtgdeckmaker.netlify.app" class=" md:absolute md:bottom-0 md:right-0">Click to View</a>
                </div>
            </div>
            <div class="md:h-96 m-4 p-2 text-justify md:grid" v-if="DisplayRotatedProjects === 2 || DisplayStaticProject === 2">
                <h4 class="text-center text-2xl md:row-start-1 md:col-start-3">Sticky Task</h4>
                <div class="md:row-start-1 md:row-end-3 md:col-start-1 md:col-end-3 h-48 md:h-full w-auto object-contain">
                    <img src="https://res.cloudinary.com/dm5cjaisp/image/upload/v1607391604/Screen_Shot_2020-12-07_at_8.39.38_PM_snavw0.png" class="pr-2 h-full w-full object-contain">
                </div>
                <div class="md:relative h-72 md:h-full p-2 md:row-start-2 md:col-start-3">
                    <section class="pb-8 pt-4">A group project using React, with a rails backend; the premise is that you can create tasks likewise to "sticky notes" to be able to assign to "taskers" whether they be workers, students, or children. My work was primarily in the frontend of the project, though I did help with bug fixes from time to time on the backend of the project.</section>
                    <a href="https://sticky-task.netlify.app" class=" md:absolute md:bottom-0 md:right-0">Click to View</a>
                </div>
            </div>
            <div class="md:h-96 m-4 p-2 text-justify md:grid" v-if="DisplayRotatedProjects === 3 || DisplayStaticProject === 3">
                <h3 class="text-center text-2xl md:row-start-1 md:col-start-3">Random Card</h3>
                <div class="md:row-start-1 md:row-end-3 md:col-start-1 md:col-end-3 h-48 md:h-full w-auto object-contain">
                    <img src="https://res.cloudinary.com/dm5cjaisp/image/upload/v1600118869/Screen_Shot_2020-09-14_at_5.27.29_PM_gqngnd.png" class="pr-2 h-full md:h-96 w-full object-contain">
                </div>
                <div class="md:relative h-72 md:h-full p-2 md:row-start-2 md:col-start-3">
                    <section class="pb-8 pt-4">A Javascript program that uses a deck of cards and will deal a random card each time you click the "add a card" button.</section>
                <a href="https://pages.git.generalassemb.ly/E-Shelton98/W02D04-HW/random_imager/" class=" md:absolute md:bottom-0 md:right-0">Click to View</a>
                </div>
            </div>
        </div>
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
    }
}
</script>

<style scoped>
.fade-enter-active {
    transition: opacity 1s ease;
}


.fade-enter-from
{
    opacity: 0;
}
</style>
