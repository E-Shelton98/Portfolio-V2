<template>
    <form class="border border-gray-900 rounded-lg m-4 flex flex-col p-4" @submit.prevent="sendEmail">
        <h3 class="text-center underline text-xl mb-2">Send me an Email</h3>
        <label>Name</label>
        <input type="text" name="user_name">
        <label>Email</label>
        <input type="email" name="user_email">
        <label>Message</label>
        <textarea name="message"></textarea>
        <input class="mt-4 bg-green-500 border border-gray-500 h-8 w-full rounded-md focus:outline-none focus:ring-2 focus:ring-purple-900 focus:ring-opacity-50 focus:bg-green-300" type="submit" value="Send">
    </form>
</template>

<script>
import emailjs from 'emailjs-com'

export default {
    methods: {
        sendEmail: (e) => {
            emailjs.sendForm('contact_service', 'contact_form', e.target, 'user_aGRjpPNDuxOEGbAbOKUKU')
            .then((result) => {
                console.log('SUCCESS!', result.status, result.text)
            }, (error) => {
                console.log('FAILED...', error)
            })
        }
    }
}
</script>