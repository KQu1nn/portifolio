<script setup>
    import HeadContainer from './HeadContainer.vue'
    import Card from './Card.vue'

    import {ref} from 'vue'

    const title = ref(`[Works & Projects]`)
    const subTitle = ref('My latest projects')
    const description = ref(`See some of the work I've developed throughout my career as a front-end programmer:`)
</script>

<template>
    <main>
        <div id="main">
            <div id="head">
                <HeadContainer :title="title" :subTitle="subTitle" :description="description"/>
            </div>
            <div class="cards">
                <Card />
                <Card />
                <Card />
                <Card />
                <Card />
                <Card />
            </div>
        </div>
    </main>
</template>

<style scoped>
    main {
        width: 100%;
        height: auto;

        display: flex;
        justify-content: center;
    }
    #main {
        width: 71%;
        padding: 0 50px;
        height: auto;

        animation-name: loadPage;
        animation-duration: 0.6s;
        animation-timing-function: ease;
    }
    #head {
        padding: 50px 0;
    }
    .cards {
        display: flex;
        justify-content: space-around;
        gap: 10px;
        flex-wrap: wrap;

        padding-bottom: 30px;
    }

    @media screen and (max-width: 600px) {
        #main {
            width: 100%;
            text-align: center
        }
        
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