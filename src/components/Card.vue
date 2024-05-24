<script setup>

</script>
<template>
    <div class="card">
        <div id="image"></div>
        <div id="description">
            <h3>UI/UX Components</h3>
            <p>Lorem consectetur adipisicing elit. ipsum dolor sit amet  adipisicing consectetur adipisicing elit. elit. A facilis repellendus voluptas neque distinctio sequi... </p>
        </div>
    </div>
</template>
<style scoped>
    .card {
        width: 270px;
        height: 380px;

        padding: 10px;

        border-radius: 10px;
        background-color: white;
        
        cursor: pointer;
    }
    #image {
        width: 100%;
        height: 180px;

        border-radius: 10px 10px 0 0;
        background-color: rgb(153, 153, 153);
    }
    #description {
        width: 100%;
        height: auto;
        
        padding: 5px 0 2px 2px;
    }
    #description h3 {
        padding: 10px 0;
        color: rgb(52, 52, 52);
    }
    #description p {
        font-size: 14px;
        color: #585858;
        line-height: 17px;
    }
    @media screen and (max-width: 500px) {
        #description p {
        font-size: 12px;
        color: #585858;
    }
        .card {
            width: 90%;
        }
    }
</style>