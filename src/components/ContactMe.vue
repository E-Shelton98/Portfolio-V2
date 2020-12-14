<template>
    <form class="border border-gray-900 rounded-lg m-4 flex flex-col" @submit.prevent="sendEmail">
        <label>Name</label>
        <input type="text" name="user_name">
        <label>Email</label>
        <input type="email" name="user_email">
        <label>Message</label>
        <textarea name="message"></textarea>
        <input type="submit" value="Send">
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