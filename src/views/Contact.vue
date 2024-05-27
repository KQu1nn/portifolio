<script setup>
    import { ref } from 'vue';
    import Header from '@/components/Header.vue';
    import HeadContainer from '@/components/HeadContainer.vue';
    import axios from 'axios';

    const title = ref(`[Contact]`)
    const subTitle = ref('Send us a message')
    const description = ref(`Let's chat. Tell me about your project.`)

    const fullName = ref('');
    const email = ref('');
    const subject = ref('');
    const textarea = ref('');

    const sendMessage = () => {
        const formData = {
            fullName: fullName.value,
            email: email.value,
            subject: subject.value,
            textarea: textarea.value
        }
        axios.post('localhost:5173/api/contact');
    }

</script>
<template>
    <main>
        <Header />
        <div class="section">
            <div id="headContainer">
                <HeadContainer :title="title" :subTitle="subTitle" :description="description"/>
            </div>
            <form @submit.prevent="sendMessage">
                <input v-model="fullName" key="fullName" type="text" placeholder="Full name*">
                <input v-model="email" key="email" type="text" placeholder="E-mail Adress">
                <input v-model="subject" key="subject" type="text" placeholder="Subject">
                <div>
                    <p>Tell us more about your project*</p>
                    <textarea v-model="textarea" key="textarea" cols="40" rows="5"></textarea>
                </div>
                <button type="submit">Send Message</button>
            </form>
        </div>
    </main>
</template>
<style scoped>
main {
  width: 100%;
  min-height: 100vh;
}
textarea {
    margin-top: 10px;
}
#fullMessage {
    padding: 10px;
}
#headContainer {
    width: 67%;
    height: auto;
    margin-bottom: 10px;
    padding: 0 10%;
}
.section {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 2rem;
  animation-name: loadPage;
  animation-duration: 0.8s;
}

form {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  width: 100%;
  max-width: 600px;
  padding: 30px 0;
}

input, textarea {
  width: 100%;
  padding: 0.5rem;
  border: 1px solid #ccc;
  border-radius: 4px;
}

button {
  padding: 0.75rem;
  background-color: #007BFF;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  font-size: 1rem;
}

button:hover {
  background-color: #0056b3;
}
p {
    color: #a7b3e0;
}
textarea:focus, input:focus, select:focus {
    outline: 0;
} 
@keyframes loadPage {
    from {
        margin-left: -170%;
    }
    to {
        margin-left: 0;
    }
}
</style>