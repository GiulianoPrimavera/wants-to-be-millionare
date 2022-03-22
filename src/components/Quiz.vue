<template>
  <div class="quiz_container">

    <div class="q_n_a_container">
        <!-- domanda --> 
        <div class="text_container question">
            <p>the quick brown fox jumps over the lazy dog</p>
        </div>

        <!-- possibili risposte -->
        <div class="answer_container">
            
            <div class="text_container answer">
                <p>the quick brown fox jumps over the lazy dog</p>
            </div>
            
            <div class="text_container answer">
                <p>the quick brown fox jumps over the lazy dog</p>
            </div>
            
            <div class="text_container answer">
                <p>the quick brown fox jumps over the lazy dog</p>
            </div>

            <div class="text_container answer">
                <p>the quick brown fox jumps over the lazy dog</p>
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
    height: 60px;
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
    border-top: 3.5px solid white;
    border-bottom: 3.5px solid white;
    border-radius: 5px;
    position: relative;
}

.text_container p::before{
    content: "";
    position: absolute;
    top: 5px;
    bottom: 0;
    left: -19px;
    border-left: 4px solid white;
    border-bottom: 4px solid white;
    width: 40px;
    height: 40px;
    transform: rotate(45deg);
    border-radius: 5px;
}
.text_container p::after{
    content: "";
    position: absolute;
    top: 5px;
    bottom: 0;
    right: -19px;
    border-right: 4px solid white;
    border-top: 4px solid white;
    width: 40px;
    height: 40px;
    transform: rotate(45deg);
    border-radius: 5px;
}
.text_container p:hover, p:hover::before, p:hover::after{
    background-color: red;
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