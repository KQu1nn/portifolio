<script setup>
    import { ref } from 'vue';
    import Header from '@/components/Header.vue';
    import HeadContainer from '@/components/HeadContainer.vue';

    const title = ref(`[Contact]`)
    const subTitle = ref('Send us a message')
    const description = ref(`Let's chat. Tell me about your project.`)
</script>
<template>
    <main>
        <Header />
        <div class="section">
            <div id="headContainer">
                <HeadContainer :title="title" :subTitle="subTitle" :description="description"/>
            </div>
            <form action="#">
                <input type="text" placeholder="Full name*">
                <input type="text" placeholder="E-mail Adress">
                <input type="text" placeholder="Subject">
                <div>
                    <p>Tell us more about your project*</p>
                    <textarea name="fulMessage" id="fullMessage" cols="40" rows="5"></textarea>
                </div>
                <button>Send Message</button>
            </form>
        </div>
    </main>
</template>
<style scoped>
main {
  width: 100%;
  min-height: 100vh;
}
#headContainer {
    width: 67%;
    height: auto;
    margin-bottom: 30px;
    padding: 0 10%;
}
.section {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 2rem;
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
</style>