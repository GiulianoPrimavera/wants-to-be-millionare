<template>
  <div class="quiz_container">

    <div class="q_n_a_container">
        <!-- domanda --> 
        <div class="text_container question">
            <p>the quick brown fox jumos over the lazy dog</p>
        </div>

        <!-- possibili risposte -->
        <div class="answer_container">
            
            <div class="text_container answer">
                <p>the quick brown fox jumos over the lazy dog</p>
            </div>
            
            <div class="text_container answer">
                <p>the quick brown fox jumos over the lazy dog</p>
            </div>
            
            <div class="text_container answer">
                <p>the quick brown fox jumos over the lazy dog</p>
            </div>

            <div class="text_container answer">
                <p>the quick brown fox jumos over the lazy dog</p>
            </div>
            
        </div>

    </div>

  </div>
</template>

<script>
export default {
name : "Quiz",
}
</script>

<style lang="css">
.quiz_container{
    background-color: darkblue;
    height: 60%;
    display: flex;
    justify-content: center;
}
p{
    color: white;
    font-size: 1.6em;
    display: inline-block;
}
.q_n_a_container{
    width: 60%;
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
}

.text_container p{
    margin: 10px;
    padding: 14px 30px;
    border: 2px solid white;
}

.text_container p::before{
    content: "";
    position: absolute;
    top: 0;
    bottom: 0;
    
}
.question{
    margin: 0 auto;
}
.answer_container{
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;

}
</style>