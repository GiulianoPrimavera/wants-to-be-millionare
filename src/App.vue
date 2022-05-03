<template>
  <main>
    <Logo></Logo>

    <Quiz :quizList="quizList"></Quiz>
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
      {
        "domanda" : "quanti numeri ha il pi greco? ",
        "risposte" : [
          {
            "risposta": "3 numeri",
            "ToF" : false
          },
          {
            "risposta": "10 000 numeri",
            "ToF" : false
          },
          {
            "risposta": "2000",
            "ToF" : false
          },
          {
            "risposta": "infiniti numeri",
            "ToF" : true
          },
        ]
      },
      {
        "domanda" : "in che anno è nato Giulietta? ",
        "risposte" : [
          {
            "risposta": "1984 a.c.",
            "ToF" : false
          },
          {
            "risposta": "anno 0",
            "ToF" : false
          },
          {
            "risposta": "2000",
            "ToF" : true
          },
          {
            "risposta": "2020",
            "ToF" : false
          },
        ]
      },
    ],
  }
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
