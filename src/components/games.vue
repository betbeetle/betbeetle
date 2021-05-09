<template>
  
    <section style="padding-bottom:10px !important">
      <b-row class="row justify-content-center">
        <b-col cols="12" md="3" lg="3" xl="3" class="mt-2">
            <b-row style="background-color:#191919 !important; border-radius:0.25rem !important; margin:1px;" >
               <b-col class="game-img text-center">
                 <b-img :src="game1" img-alt="Image" ></b-img>
                 
               </b-col>
            </b-row>
           
            <b-row  style="background-color:#2B2B2B !important; border-radius:0.25rem !important; margin:1px; padding-top:10px; ">
             
               <b-card-text>
                  <h2 class="game">Smart Betting</h2>
            <div style="display: block" class="game-text" data-aos="fade-up" data-aos-delay="200">Bet against your friends and the Betbeetle community or create your own decentralized bet on any event - crypto, sports, politics and more.</div>
            <div style="display: block; margin:1rem 0.75rem;"><a href="https://app.betbeetle.com" class="button btn-link btn-primary mt3">Play now</a></div>
          </b-card-text>
            </b-row>
        </b-col>

        <b-col cols="12" md="3" lg="3" xl="3"  class="mt-2">
           <b-row style="background-color:#191919 !important; border-radius:0.25rem !important; margin:1px; " >
               <b-col class="game-img text-center">
                 <b-img :src="game2" img-alt="Image" ></b-img>              
               </b-col>
            </b-row>
             <b-row style="background-color:#2B2B2B !important; border-radius:0.25rem !important; margin:1px; padding-top:10px; ">
           <b-card-text   > 
             <h2 class="game">Beetle Lotto</h2>
            <div style="display: block" class="game-text" data-aos="fade-up" data-aos-delay="200">Be the lucky winner when the bought back BEETLE tokens are distrubuted regularly. What do you need to do for it? Just get Betbeetle Premium!</div>
            <div style="display: block; margin:1rem 0.75rem;"><a href="https://app.betbeetle.com" class="button btn-link btn-primary mt3">Play now</a></div>
          </b-card-text>
           </b-row>
        </b-col>

        <b-col cols="12" md="3" lg="3" xl="3" class="mt-2">
         <b-row style="background-color:#191919 !important; border-radius:0.25rem !important; overflow: hidden !important; margin:1px;" >
            <b-col class="game-img text-center">
              <b-img :src="game3" ></b-img>
            </b-col>
          </b-row>
          <b-row style="background-color:#2B2B2B !important; border-radius:0.25rem !important; margin:1px; padding-top:10px; ">
             <b-card-text>
               <h2 class="game">Pepe Hangman</h2>
            <div style="display: block" class="game-text" data-aos="fade-up" data-aos-delay="200">Play the famous game Hangman against your friends on the blockchain with crypto. Currently in development.</div>
            <div style="display: block; margin:1rem 0.75rem;"><a href="#" class="button btn-link btn-primary mt3">Coming soon</a></div>
          </b-card-text>
          </b-row>

        </b-col>

        <b-col cols="12" md="3" lg="3" xl="3" class="mt-2">
          <b-row style="background-color:#191919 !important; border-radius:0.25rem !important; overflow: hidden !important; margin:1px;" >
            <b-col class="game-img text-center">
              <b-img :src="game4" ></b-img>
            </b-col>
          </b-row>
          <b-row style="background-color:#2B2B2B !important; border-radius:0.25rem !important; margin:1px; padding-top:10px; ">
            <b-card-text>
              <h2 class="game">Spin the bottle</h2>
            <div style="display: block" class="game-text" data-aos="fade-up" data-aos-delay="200">Spin the bottle together with your friends and make them fulfill crypto tasks. Currently in development.</div>
            <div style="display: block; margin:1rem 0.75rem; "><a href="#" class="button btn-link btn-primary mt3">Coming soon</a></div>
          </b-card-text>
          </b-row>
        </b-col>
      </b-row>
      
  </section>

</template>

<script>
import { BCardText } from 'bootstrap-vue'

export default {
  name: 'home',
  components: {
    BCardText
  },
  data () {
    return {
      game1: require('@/assets/img/game_betting.png'),
      game2: require('@/assets/img/game_beetle-jackpot.png'),
      game3: require('@/assets/img/game_hanging-pepe.png'),
      game4: require('@/assets/img/game_bottle.png'),
      // card item Arrey

      // cardItems: [{heading: 'simply dummy text of the printing 1', paragraph: 'is simply dummy text of the printing and typesettin dummy text of the printing and typesettin dummy text of the printing and typesetting', img: require('@/assets/img/ia_100000030.png')}, {heading: 'simply dummy text of the printing 1', paragraph: 'is simply dummy text of the printing and typesetting', img: require('@/assets/img/ia_100000030.png')}, {heading: 'simply dummy text of the printing 1', paragraph: 'is simpldummy text of the printing and typesettindummy text of the printing and typesettiny dummy text of the printing and typesetting', img: require('@/assets/img/ia_100000030.png')}]

    }
  }
}
</script>
<style scoped>
.card-title {
  font-size:30px;
  font-weight:bold;
  color:#fff;
}
.game-img img {
  width:100%;
}
@media screen and (min-width:768px) {
  .hidden-lg{
		display: none;
	}
  .game-bottom {
    font-size: 0.8em;
    margin-top: 0;
    margin: 5%;
    margin-bottom: 1em;
    font-weight: 500;
  }
  .game {
    font-size: 1em !important;
    font-weight: 400  !important;
    margin: 5%;
    margin-top: 8px;
    
    font-family: 'Roboto', serif;
  }
   .game-text {
    font-size: 0.9em !important;
    height: 100px;
    font-weight: 400  !important;
    margin: 5%;
    margin-top: 8px;
    overflow: hidden;
    font-family: 'Roboto', serif;
    
  }
}
@media screen and (max-width:600px) {
  .game-img{
    padding:3px;
    width:100%
  }
  .game-bottom {
    font-size: 0.8em;
    margin-top: 0;
    margin-left: 5%;
    margin-bottom: 1em;
    font-weight: 500;
     font-family: 'Roboto', serif;
     color:#ffffff;
     height: 55px;
     overflow: hidden;
  }
  .game {
    font-size: 1em !important;
    font-weight: 400  !important;
    margin: 5%;
    margin-top: 8px;
    
    font-family: 'Roboto', serif;
  }
   .game-text {
    font-size: 0.9em !important;
    font-weight: 400  !important;
    margin: 5%;
    margin-top: 8px;
    overflow: hidden;
    font-family: 'Roboto', serif;
    
  }
  
}
</style>