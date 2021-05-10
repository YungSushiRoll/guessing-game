<template>
    <div id="container">
        <header>Guess a number between 1-10!</header>
        <ion-input id="theResp"></ion-input>
        <ion-input placeholder="Enter Input" id="theGuess"></ion-input>
        <ion-button id="guessBtn" color="medium" @click="guessClick()">GUESS</ion-button>
        <ion-button id="replayBtn" color="success" @click="restartClick()">Play Again?</ion-button><br>
        <ion-button id="exitBtn" color="danger" href="/tabs/tab3">Exit?</ion-button>
    </div>
</template>

<script>
import { IonButton, IonInput } from '@ionic/vue';
export default {
    components: { IonButton, IonInput },
    created() {
        this.getRando();
    },
    data() {
        return {
            rand : "",
            count: 0,
            guess : ""
        }
    },
    methods: {
        guessClick(){
            const theRando = this.rand;
            this.guess = document.getElementById('theGuess').value;
            console.log(theRando + " " + this.guess)
            if (this.guess == theRando){
                document.getElementById('theResp').value = "You got it!";
                document.getElementById('guessBtn').disabled = "true";
                document.getElementById('replayBtn').style.display = "inline-block";
                document.getElementById('exitBtn').style.display = "inline-block";

            } else {
                this.count++;
                document.getElementById('theResp').value = "Oof! Guess again! Guess Count: " + this.count;
            }
        },
        restartClick()
        {
            this.getRando();
            this.resetVals();
        },
        getRando()
        {
            this.rand = Math.floor((Math.random() * 10) + 1);
            console.log(this.rand);
        },
        resetVals()
        {
            document.getElementById('guessBtn').disabled = "false";
            document.getElementById('replayBtn').style.display = "none";
            document.getElementById('exitBtn').style.display = "none";
            this.count = 0;
            document.getElementById('theGuess').value = "";
        }
    },
}
</script>

<style scoped>
#replayBtn, #exitBtn {
    display: none;
}
#container {
  text-align: center;
  position: absolute;
  left: 0;
  right: 0;
  top: 50%;
  transform: translateY(-50%);
}

#container strong {
  font-size: 20px;
  line-height: 26px;
}

#container p {
  font-size: 16px;
  line-height: 22px;
  color: #8c8c8c;
  margin: 0;
}

#container a {
  text-decoration: none;
}
</style>