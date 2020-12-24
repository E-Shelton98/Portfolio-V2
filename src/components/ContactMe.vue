<template>
    <form class="border border-gray-900 rounded-lg mt-4 lg:mx-32 flex flex-col p-4" @submit.prevent="sendEmail">
        <h3 class="text-center underline text-xl mb-2">Send me an Email</h3>
        <label>Name</label>
        <input class="w-72" type="text" name="user_name">
        <label>Email</label>
        <input class="w-72" type="email" name="user_email">
        <label>Message</label>
        <textarea name="message"></textarea>
        <input class="text-white mt-4 bg-purple-300 border border-gray-500 h-8 w-full rounded-md focus:outline-none focus:ring-2 focus:ring-black focus:ring-opacity-50 focus:bg-gray-300" type="submit" value="Send">
        <section class="" v-if="EmailSent">Email Sent!</section>
    </form>
    <div class="border border-gray-900 rounded-lg mt-4 lg:mx-32">
            <section class="m-2 text-center text-xl underline">Socials</section>
            <div class="flex flex-col md:flex-row justify-around"><section class="m-1 text-center">View my <a href="https://github.com/E-Shelton98" class="underline">GitHub</a></section>
            <section class="m-1 text-center">Connect on <a href="https://www.linkedin.com/in/erik-shelton-07a932192/" class="underline">LinkedIn</a></section></div>
        </div>
</template>

<script>
import emailjs from 'emailjs-com'

export default {
    
    name: 'ContactMe',
    data () {
        return {
            EmailSent: false
        }
    },
    methods: {
        sendEmail(e) {
            emailjs.sendForm('contact_service', 'contact_form', e.target, 'user_aGRjpPNDuxOEGbAbOKUKU')
            .then(() => {
                this.test()
            }, (error) => {
                console.log('FAILED...', error)
            })
        },
        test() {
            this.EmailSent = true
        }
    }
}
</script>