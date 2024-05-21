<script setup>

</script>
<template>
    <div id="main">
        <div id="container">
            <p id="p1">Hi, my name is</p>
            <div>
                <p class="p2">Ramon Kelvin.</p>
                <p class="p2" id="p2">I build things for the web.</p>
            </div>   
            <p id="p3">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Et sed deserunt qui deleniti porro optio eligendi sint provident amet facere architecto dignissimos, tempore quas debitis</p>
            <button>
                Check out my course!
            </button>
        </div>
    </div>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Fira+Code:wght@300..700&family=Fira+Sans:ital,wght@0,100;0,200;0,300;0,400;0,500 ;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&family=Karla:ital,wght@0,200..800;1,200..800&display=swap');
#main {
    width: 100%;
    height: auto;
    display: flex;
    justify-content: center;

    font-family: "Karla";
}
#container {
    width: 55%;
    height: auto;
    display: flex;
    flex-direction: column;
    gap: 15px;
    padding: 60px 0;

    animation-name: loadPage;
    animation-duration: 0.6s;
    animation-timing-function: ease;
}
#p1 {
    font-size: 14px;
    color: #57c586;
}
.p2 {
    font-size: 45px;
    font-weight: 600;
    color: #ccd6f6;
}
#p2 {
    color: #8891b0;
}
#p3 {
    font-size: 12px;
    width: 60%;
    padding: 10px 0;
    color: #6a718a;
}
button {
    width: 190px;
    background-color: transparent;
    border: solid 1px #57c586;
    border-radius: 5px;
    padding: 10px;
    color: #57c586;
    cursor: pointer;
    margin-top: 10px;
}
button:hover {
    background-color: #57c586;
    color: #15173d;
    font-weight: 600;
    transition: background-color 0.3s, color 0.3s;
}

@media screen and (max-width: 600px) {
  .p2 {
    font-size: 35px;
  }
  #container {
    width: 80%;
    padding: 100px 0;
  }
  #p2 {
    font-size: 16px;
    padding: 15px 0;
  }
  #p3 {
    width: 100%;
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