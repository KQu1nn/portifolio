<script setup>
    const props = defineProps({
        title: String,
        subTitle: String,
        description: String,
    });
</script>
<template>
    <div id="wrapper">
        <h2>{{ title }}</h2>
        <h3>{{ subTitle }}</h3>
        <p id="description">{{ description }}</p>
    </div>
</template>
<style scoped>
    #wrapper {
        width: 100%;
        height: auto;
        
        padding: 10px 0;

        display: flex;
        justify-content: center;
        flex-direction:column;
        gap: 14px;
    }
    #wrapper h2 {
        color: #60d090;
    }
    #wrapper h3 {
        color: #b5c1ed;
    }
    #wrapper p {
        font-size: 14px;
        color: #8990aa;
    }
    
    @media screen and (max-width: 500px) {
        #wrapper {
        display: flex;
        justify-content: center;
        align-items: center;
    }
    #wrapper h3 {
        text-align: center;
        font-size: 16px;
    }
    #wrapper p {
        text-align: center;
    }
}
</style>