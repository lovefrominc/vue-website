<template>
  <section id="main" class="container">
    <h1>Welcome to LoveFrom Inc.</h1>
    <br>
    <h3>It's very easy to be different, but very difficult to be better.</h3>
    <p>- Jony Ive</p>
  </section>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "home"
};
</script>
<style>
#main{
    height: calc(100vh - 324px);
    display: flex;
    flex-direction: column;
    justify-content: center;
}
#main h1{
    font-size: 32px;
    font-weight: normal;
    color: #2a2a2a;
}
#main h3{
    font-size: 20px;
    font-weight: normal;
    color: #2a2a2a
}
#main::after{
    display: none;
}
@media screen and (min-width: 768px){
  #main::after{
    content: " ";
    width: 30%;
    height: 30%;
    display: block;
    position: absolute;
    color: #2a2a2a;
    font-size: 48px;
    background-image: url("~@/assets/shade.png");
    background-position: center;
    background-size: 300px 300px;
    opacity: 0.2;
    background-repeat: no-repeat;
    right: 2%;
    top: calc(50% - 175px)
  }
}
</style>
