<script setup>
    import HeadContainer from '../components/HeadContainer.vue'
    import {ref} from 'vue'

    const title = ref(`[Skill & tools]`)
    const subTitle = ref('My Toolbox & Things I Can Do')
    const description = ref(`The skills, tools and technologies I use to bring your products to life:`)
</script>
<template>
    <div id="main">
        <section>
            <HeadContainer :title="title" :subTitle="subTitle" :description="description"/>
            <div id="cards">
                <div class="card">
                    <div id="box">
                        <i class="devicon-html5-plain colored"></i>
                        <p>HTML</p>
                    </div>
                </div>
                <div class="card">
                    <div id="box">
                        <i class="devicon-css3-plain colored"></i>
                        <p>CSS</p>
                    </div>
                </div>
                <div class="card">
                    <div id="box">
                        <i class="devicon-javascript-plain colored"></i>
                        <p>Javascript</p>
                    </div>
                </div>
                <div class="card">
                    <div id="box">
                        <i class="devicon-tailwindcss-original colored"></i>
                        <p>Tailwind</p>
                    </div>
                </div>
                <div class="card">
                    <div id="box">
                        <i class="devicon-vuejs-plain colored"></i>
                        <p>VueJS</p>
                    </div>
                </div>
                <div class="card">
                    <div id="box">
                        <i class="devicon-git-plain colored"></i>
                        <p>Git</p>
                    </div>
                </div>
                <div class="card">
                    <div id="box">
                        <i class="devicon-github-plain colored"></i>
                        <p>GitHub</p>
                    </div>
                </div>
                <div class="card">
                    <div id="box">
                        <i class="devicon-vitejs-plain colored"></i>
                        <p>ViteJS</p>
                    </div>
                </div>
                <div class="card">
                    <div id="box">
                        <i class="devicon-sass-original colored"></i>
                        <p>SASS</p>
                    </div>
                </div>

                <div class="card">
                    <div id="box">
                        <i class="devicon-visualstudio-plain colored"></i>
                        <p>VS Code</p>
                    </div>
                </div>
            </div>
            <div id="boxDescription">
                <h3>[Currenty working on]</h3>
                <p>Improving my skill in, and understanding of vanilla Javascript and VueJS. Also, having fun with #100DaysOfCode building & animating things via CSS. <a>Follow my journey here.</a></p>
            </div>
        </section>
    </div>
</template>
<style scoped>
#main {
    width: 100%;
    height: 10%;
    display: flex;
    justify-content: center;
}
section {
    width: 70%;
    height: auto;

    margin: 50px 0;
    padding: 15px 40px;

    display: flex;
    flex-direction:column;
    gap: 40px;

    animation-name: loadPage;
    animation-duration: 0.6s;
    animation-timing-function: ease;
}

#cards {
    width: 100%;
    height: 100%;

    display: grid;
    grid-template-columns: repeat(5, 1fr);

}
.card {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: start;
    padding-left: 5px;
    cursor: pointer;
}
#box {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 10px;
    padding: 15px 0;
}
#box p {
    color: #a7b3e0;
}
#boxDescription {
    width: 90%;
    height: auto;
}
#boxDescription h3 {
    color: #b5c1ed;
    padding: 15px 0;
}
#boxDescription p {
    color: #8990aa;
    font-size: 14px
}
i {
    font-size: 70px;
}
h2 {
    font-weight: 500;
}
a {
    color:#57c586;
}

@media screen and (max-width: 600px) {
    section {
        width: 100%;
    }
    #description {
        width: 100%;
        display: flex;
        text-align: center;
    }
    #boxDescription {
        width: 100%;
        padding-bottom: 50px;
    }
    #boxDescription h3 {
        text-align: center;
        width: 100%;
    }
    #boxDescription p {
        text-align: center;
    }
}
@media screen and (max-width: 500px) {
    #cards {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
    }
    .card {
        display: flex;
        align-items: center;
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