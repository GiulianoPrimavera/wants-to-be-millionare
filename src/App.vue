<template>
  <main>
    <Logo></Logo>
  </main>
</template>

<script>
import Logo from "./components/Logo.vue"

export default {
name : "App",
components: { Logo }, 

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
