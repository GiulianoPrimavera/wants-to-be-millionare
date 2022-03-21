<template>
  <main>
    <Logo></Logo>

    <Quiz></Quiz>
  </main>
</template>

<script>
import Logo from "./components/Logo.vue"
import Quiz from "./components/Quiz.vue"

export default {
name : "App",
components: { Logo, Quiz }, 

}
</script>

<style lang="scss">
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
main{
  height: 100vh;
}
</style>
