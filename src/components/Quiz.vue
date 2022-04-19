<template>
  <div class="quiz_container">
    <div class="q_n_a_container">
      <!-- domanda -->
      <div class="text_container question">
        <p>{{ currentQuiz[0].domanda }}</p>
      </div>

      <!-- possibili risposte -->
      <div class="answer_container">
        <div
          class="text_container answer"
          v-for="risposta in currentQuiz[0].risposte"
          :key="risposta.id"
        >
          <p>{{ risposta.risposta }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
name : "Quiz",
props : {
    quizList: Array
},
data(){
    return{
        currentQuiz: []
    }
},
methods: {
    /**
     * questa funzione recupera un solo set di domanda e risposta in modo da stamparla singolarmente
    */ 
    getSingleQuiz(){
        //dall'array completo dei quiz devo tagliare una domanda e incollarla nel currentQuiz
        const rand = Math.floor(Math.random() * this.quizList.length);

        //qui vado a recuperare la domanda random dall'array di domande
        this.currentQuiz = this.quizList.slice(rand, rand + 1);
        console.log(this.currentQuiz[0].risposte);

        this.shuffleArray(this.currentQuiz[0].risposte);
    },
    /**
     * funzione che mischia elementi all'interno di un array (spudoratamente copiata da stack over flow)
     */
    shuffleArray(array) {
        let currentIndex = array.length,  randomIndex;

        // While there remain elements to shuffle.
        while (currentIndex != 0) {

            // Pick a remaining element.
            randomIndex = Math.floor(Math.random() * currentIndex);
            currentIndex--;

            // And swap it with the current element.
            [array[currentIndex], array[randomIndex]] = [
            array[randomIndex], array[currentIndex]];
        }

        return array;
    }
},
beforeMount(){
    this.getSingleQuiz();
}
}
</script>

<style>
</style>