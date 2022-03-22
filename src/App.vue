<template>
  <main>
    <Logo></Logo>

    <Quiz :quizList="quizList[0]"></Quiz>
  </main>
</template>

<script>
import Logo from "./components/Logo.vue"
import Quiz from "./components/Quiz.vue"

export default {
name : "App",
components: { Logo, Quiz }, 
data(){
  return{
    // qui dovrò scrivere un array di oggetti, ogni oggetto avra: domanda, risposte. ogni risposta avrà del testo e se sia quella vera o falsa
    quizList: [
      {
        "domanda" : "quanto fa 2 + 2 ? ",
        "risposte" : [
          {
            "risposta": "3",
            "ToF" : false
          },
          {
            "risposta": "2",
            "ToF" : false
          },
          {
            "risposta": "2000",
            "ToF" : false
          },
          {
            "risposta": "4",
            "ToF" : true
          },
        ]
      },
    ]
  }
},
methods:{
  prova(){
    console.log(this.quizList[0]);

  }
},
mounted(){
  this.prova()
}

}
</script>

<style lang="scss">
@import "styles/quiz.scss";

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
main{
  height: 100vh;
}

</style>
