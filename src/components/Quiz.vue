<template>
  <div class="quiz_container">

    <div class="q_n_a_container">
        <!-- domanda --> 
        <div class="text_container question">
            <p>{{quizList.domanda}}</p>
        </div>

        <!-- possibili risposte -->
        <div class="answer_container">
            
            <div class="text_container answer" v-for="risposta in quizList.risposte" :key="risposta.id">
                <p>{{risposta.risposta}}</p>
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
}
}
</script>

<style>

</style>