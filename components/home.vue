<template>
  <div class="main-div">
  
    <!--header Section --> 
    <section>
    <b-row style="background-color: #212121" class="row justify-content-center">
      
      <b-col class="min-heading" style="" md="7" lg="7" sm="12" xl="7">
		
		  <b-row>
    <b-col cols="12" md="12" lg="12" xl="12"> <b-img
          alt="Betbeetle.com - Official Website"
          title="Betbeetle.com - Official Website"
          style="display: block; margin:0 auto"
          :src="logo"
        ></b-img>
		</b-col>
    
    <b-col cols="12" md="12" lg="12" xl="12"><h1
          class="mt-12 heading-title"
          style="display: block; color:#fff;"
        >
          Maximize your <span style="color:red !important;">crypto</span> gains through social competition and passive rewards.
        </h1></b-col>
		<b-col>
			 <p cols="12"  md="12" lg="12" xl="12">
          Smart multichain betting combined with passive income streams and never ending 7% passive rewards through static reflection - decentralized, instant, no registration. Connect your wallet and challenge your friends and our community!
        </p>
		</b-col>
  </b-row>
       
		
        
       
      
        <b-row class="row justify-content-center">
          <b-col class="row justify-content-center">

            <a href="https://exchange.pancakeswap.finance/#/swap?inputCurrency=0xbb4CdB9CBd36B01bD1cBaEBF2De08d9173bc095c&outputCurrency=0x5f588B4Cc001fbB1A572eD5AaEA265BfEA251385" style="color:#fff !important;">
            <button
              class="button mt-3 btn-primary"
              block
            >
              Buy BEETLE   
            </button>
            </a>
            <a href="https://app.betbeetle.com">
            <button
              class="button-outlated2 wp mt-3"
              block
            >
              <span style="color:red !important;">Open App</span>
            </button>
            </a>
          </b-col>
        </b-row>
        <div class="text-center mt-3"><small>Contract: <span class="pointer" style="color:#fff" @click="copy('0x5f588b4cc001fbb1a572ed5aaea265bfea251385')">0x5f588b4cc001fbb1a572ed5aaea265bfea251385</span></small></div>
      </b-col>
    </b-row>
    </section>

    <games />

    <!-- animated Section -->
    <section style="padding-top:10px !important">
    <div data-aos="fade-up" data-aos-delay="200" class="justify-content-center mt-3">

        <div style="padding:1rem !important; background:#4A1B21 !important; padding: 5rem 2rem  !important">
			<b-row>
				<b-col cols="12" sm="12" md="4" lg="4" data-aos="fade-up" data-aos-delay="200" style="background:#4A1B21 !important; padding:25px; width:90%">
					<b-img
						
						alt="Betbeetle cool frog"
						title="Betbeetle cool frog"
						class="fire-move img-size"
						:src="claimLeft"
					>
					</b-img>
					<div class="shape-up shape-up-heigh"></div>
				</b-col>
				<b-col cols="12" sm="12" md="8" lg="8"  class="content">
					<h2 style="padding-left:0;" >BEETLE Premium</h2>  
					<p style="text-align: left; margin-left:0;max-width:80%;">
						Buy and hold at least <strong>100 000 000 000</strong> BEETLE in your own wallet to activate Beetle Premium. With Beetle Premium, you:<br /><br />
						<ul class="ullist">
							<li> get <strong>82% of all platform fees</strong> that are shared among Beetle Premium wallets in BNB.</li>
							<li> automatically participate in the Beetle Lotto where <strong>10% of all platform fees</strong> are being used to buy back BEETLE tokens regularly and then being distributed to one lucky winner.</li>
							<li> always get 100% margin for every bet that you win.</li>
              <li> are able to withdraw the winnings from all games on Betbeetle - Beetle Premium is a must for that.</li>
						</ul>
            Moreover, 7% of all buys and sells are reflected among all BEETLE holders. Another 7% of all buys and sells contribute towards automatically generating liquidiy locked inside PancakeSwap V2.
					</p>
					<b-row class="row justify-content-center mt-5">
						<b-col cols="6" sm="12" md="6" lg="6">
							<button class="button-outlated">
							<p>TOTAL SUPPLY</p>	1000T BEETLE
								
							</button>
						
						</b-col>
						<b-col cols="6"  md="6" lg="6">
							<button class="button-outlated">
							<p>PREMIUM</p>0.1T BEETLE
								
							</button>
						
						</b-col>
					</b-row>
					<b-row class="row justify-content-center">
						
					</b-row>
				</b-col>
			</b-row>
        </div>
    </div>
    </section>

    <!-- section video @@ card-->
    <section data-aos="fade-up" data-aos-delay="200">
      <b-row class="video-top circular justify-content-center">
        <b-col cols="12" md="7" lg="7" xl="7" class="action-work">
          <h2 class="text-center content-video" style="margin-top:3rem; color: #fff">
            How does Betbeetle work? <i class="fas fa-briefcase mx-3" style="color:red; "></i>
          </h2>
          <p class="center content-video-text text-center">
            Learn more on how you create new bets, participate in existing bets and level up to maximize your betting profits. Find out about the RFI Static Rewards, the automatic LP and read more on our plans for the future.
          </p>
          <p class="center text-center">
          <button
            class="button mt-3 btn-primary"
            block
            style="background-color: #ca0007 !important"
            @click="forward('https://www.medium.com/betbeetle')"
          >
            Blog
          </button>
          <button
              class="button-outlated2 wp mt-3"
              block
            >
              <a href="/whitepaper.pdf"><span style="color:red !important;"> Whitepaper</span></a>
            </button>
          </p>
        </b-col>
		<b-col class="hidden-lg" cols="3" md="0" lg="0" xl="0"></b-col>
        <b-col  cols="12" md="5" lg="5" xl="5" align-self="end" class="video-small pl-5">
          <b-row>
            <b-col cols="12">
              <b-img 
          alt="Video on Betbeetle"
          title="Video on Betbeetle" :src="video"> </b-img>
            </b-col>
            <b-col cols="12" class="videobutton">
              <div class="shape" v-b-modal.modal-center>
                <b-img
          alt="Video button on Betbeetle"
          title="Video button on Betbeetle"
                  :src="videoButton"
                  style="width: 68px"
                  rounded="circle"
                ></b-img>
              </div>
            </b-col>
          </b-row>
        </b-col>
      </b-row>
      <b-img :src="auctionWork" 
	  class="d-none d-sm-block"
          alt="Beetles walk on Betbeetle"
          title="Beetles walk on Betbeetle"></b-img>
		  
      <b-container>
        <!-- Grid column -->


        <b-modal hide-footer hide-header id="modal-center" centered>
          <div class="video-modal">
            <iframe
              style="width: 460px; height: 300px"
              src="https://www.youtube.com/embed/9SGHYe6VIrs"
              allowfullscreen
            ></iframe>
          </div>
        </b-modal>
      </b-container>
      <b-row>
        <b-col md="5" lg="5" sm="5" class="d-none d-md-block"> </b-col>
        <b-col
          cols="12"
          md="2"
          lg="2"
          sm="2"
          class="d-none d-md-block rocket-col vert-move row justify-content-center"
        >
          <b-img class="rocke-img" 
          alt="Betbeetle rocket"
          title="Betbeetle rocket" :src="rocket"></b-img>
        </b-col>
        <b-col md="5" lg="5" cols="" class="d-none d-md-block"> </b-col>
      </b-row>



      <b-row class="row justify-content-center breck">
        <b-col cols="6" md="6"  lg="6" class="content-action  action text-center">
         <b-row class="row justify-content-center">
			 <b-col cols="10" md="12"  lg="12" xl="12" class="content-card ml-2">
				  <b-img class="img-content" alt="Betbeetle smartphone"
          title="Betbeetle smartphone" style="" :src="auctionContentRightCol1"> </b-img>
		  		<b-row>
					  <b-col cols="4" class="hidden-lg">
						  <span style="width:40px !important;"><h3 style="background-color:red !important; border-radius:10px; !important">1</h3></span>
					  </b-col>
				  </b-row>
			 </b-col>
		 </b-row>

		 
          <h2 class="text-center content-video">Buy BEETLE</h2>
          <p class="text-center content-video-text">
            It's not a must to play but it's highly recommended to buy and hold some Beetle on your own wallet to <strong>activate BEETLE</strong> Premium before you start creating and placing your own bets.
          </p>
          <p>
          <button
            class="button mt-3 btn-primary"
            block
          >
          <a href="https://exchange.pancakeswap.finance/#/swap?inputCurrency=0xbb4CdB9CBd36B01bD1cBaEBF2De08d9173bc095c&outputCurrency=0x5f588B4Cc001fbB1A572eD5AaEA265BfEA251385">
            Buy $BEETLE
          </a>
          </button>
          </p>
        </b-col>
        <b-col md="1" sm="1" lg="1" class="content-border d-none d-md-block">
          <div class="box-top"></div>
        </b-col>

        <b-col cols="6" md="5" sm="5" lg="5" class="content-action action text-center">
			 <b-img :src="auctionWork" 
			 class="action-img hidden-lg"
          alt="Beetles walk on Betbeetle"
          title="Beetles walk on Betbeetle"></b-img>
        </b-col>
      </b-row>

 
      <b-row class="row justify-content-center">
		   <b-col cols="6" md="5" sm="5" lg="5" class="content-action action text-center hidden-lg">
			 <b-img  :src="auctionWork" 
			 class="action-img"
          alt="Beetles walk on Betbeetle"
          title="Beetles walk on Betbeetle"></b-img>
        </b-col>
        <b-col cols="6" md="6"  lg="6" class="content-action  action text-center hidden-lg">
         <b-row class="row justify-content-center">
			 <b-col cols="10" md="12"  lg="12" xl="12" class="content-card ml-2">
				  <b-img class="img-content" alt="Betbeetle smartphone"
          title="Betbeetle smartphone" style="" :src="auctionContentLeftCol2"> </b-img>
		  		<b-row>
					  <b-col cols="4">
						  <span style="width:40px !important;"><h3 style="background-color:red !important; border-radius:10px; !important">2</h3></span>
					  </b-col>
				  </b-row>
			 </b-col>
		 </b-row>

		 
          <h2 class="text-center content-video">Start winning</h2>
          <p class="text-center content-video-text">
            Open our application, connect your wallet and create your own new bet or participate in existing bets on crypto, sports or even politics - it's 100% free.
          </p>
          <p>
          <button
            class="button mt-3 btn-primary"
            block
          >
          <a href="https://app.betbeetle.com">
             Open App
          </a>
          </button>
          </p>
        </b-col>
		<b-col lg="6" md="6" xl="6"></b-col>
        <b-col md="1" sm="1" lg="1" class="content-border d-none d-md-block">
          <div class="box-top"></div>
        </b-col>  

		<b-col cols="6" md="5"  lg="5" xl="5" class="content-action  action text-center hidden-sm">
         <b-row class="row justify-content-center">
			 <b-col cols="10" md="12"  lg="12" xl="12" class="content-card ml-2">
				  <b-img class="img-content" alt="Betbeetle smartphone"
          title="Betbeetle smartphone" style="" :src="auctionContentLeftCol2"> </b-img>
		  		<b-row>
					  <b-col cols="4" class="hidden-lg">
						  <span style="width:40px !important;"><h3 style="background-color:red !important; border-radius:10px; !important">2</h3></span>
					  </b-col>
				  </b-row>
			 </b-col>
		 </b-row>

		 
          <h2 class="text-center content-video">Start winning</h2>
          <p class="text-center content-video-text">
            Open our application, connect your wallet and create your own new bet or participate in existing bets on crypto, sports or even politics - it's 100% free.
          </p>
          <p>
          <button
            class="button mt-3 btn-primary"
            block
          >
             <a href="https://app.betbeetle.com">
             Open App
          </a>
          </button>
          </p>
        </b-col>  
      </b-row>


	  
      <b-row class="row justify-content-center">
        <b-col cols="6" md="6"  lg="6" class="content-action  action text-center">
         <b-row class="row justify-content-center">
			 <b-col cols="10" md="12"  lg="12" xl="12" class="content-card ml-2">
				  <b-img class="img-content" alt="Betbeetle smartphone"
          title="Betbeetle smartphone" style=""  :src="auctionWin"> </b-img>
		  		<b-row>
					  <b-col cols="4" class="hidden-lg">
						  <span style="width:40px !important;"><h3 style="background-color:red !important; border-radius:10px; !important">3</h3></span>
					  </b-col>
				  </b-row>
			 </b-col>
		 </b-row>

		 
          <h2 class="text-center content-video">Hold and earn</h2>
          <p class="text-center content-video-text">
            Hold your BEETLE and stay with us to earn 82% of all Platform Fees, 7% RFI Static Rewards, participate in the Beetle Lotto for free - and make new crypto friends in our community!
          </p>
          <p>
          <button
            class="button mt-3 btn-primary"
            @click="forward('https://t.me/betbeetle')"
            block
          >
            Join Telegram
          </button>
          </p>
        </b-col>
        <b-col md="1" sm="1" lg="1" class="content-border d-none d-md-block">
          <div class="box-top"></div>
        </b-col>

        <b-col cols="6" md="5" sm="5" lg="5" class="content-action action text-center">
			
			 <b-img :src="auctionWork" 
			 class="action-img hidden-lg"
          alt="Beetles walk on Betbeetle"
          title="Beetles walk on Betbeetle"></b-img>
        </b-col>
      </b-row>
	 <br>
 



      <b-row d-none d-lg-block>
        <b-col class="fire d-none d-md-block" cols="12" sm="12" md="12" lg="12" style="margin-bottom: 1rem !important;">
          <b-img alt="Betbeetle beetle flying"
          title="Betbeetle beetle flying" center class="fire-move" :src="fire"> </b-img>
        </b-col>

    <b-carousel
    id="carousel-1"
    :interval="4000"
    background="transparent"
    img-height="30"
    style="margin: 0 auto !important;"
  >
      <b-carousel-slide>
        <template #img><center><b-img
              alt="Ethereum" height="30"
              title="Ethereum" :src="eth"> </b-img></center></template>
      </b-carousel-slide>
      <b-carousel-slide>
        <template #img><center><b-img
              alt="Binance Smart Chain" height="30"
              title="Binance Smart Chain" :src="bsc"> </b-img></center></template>
      </b-carousel-slide>
      <b-carousel-slide>
        <template #img><center><b-img
              alt="Huobi ECO Chain" height="30"
              title="Huobi ECO Chain" :src="heco"> </b-img></center></template>
      </b-carousel-slide>
      <b-carousel-slide>
        <template #img><center><b-img
              alt="XDAI" height="30"
              title="XDAI" :src="xdai"> </b-img></center></template>
      </b-carousel-slide>
      <b-carousel-slide>
        <template #img><center><b-img
              alt="Arbitrum" height="30"
              title="Arbitrum" :src="arb"> </b-img></center></template>
      </b-carousel-slide>
      <b-carousel-slide>
        <template #img><center><b-img
              alt="Polygon" height="30"
              title="Polygon" :src="polygon"> </b-img></center></template>
      </b-carousel-slide>
    </b-carousel>
      </b-row>
    </section>
  </div>
</template>

<script>

import { BCarousel, BCarouselSlide, BModal } from 'bootstrap-vue'

export default {
  name: 'home',
  components: { BCarousel, BCarouselSlide, BModal, games: () => import("@/components/games.vue") },
  data () {
    return {
      showModal: false,
      numbeCheck: 0,
      amount: 0,
      hoverValue: true,
      noMetamask: false,
      noMetamaskDesktop: false,
      buttontext: 'Install Metamask now',
      publicPath: process.env.BASE_URL,
      cssProps: {
      },
      bets: {},
      token: [],
      cats: [],
      // image import from assets and reaname there
      game1: require('@/assets/img/game_betting.png'),
      game2: require('@/assets/img/game_beetle-jackpot.png'),
      game3: require('@/assets/img/game_hanging-pepe.png'),
      game4: require('@/assets/img/game_bottle.png'),
      logo: require('@/assets/img/beetlemoney.png'),
      videoButton: require('@/assets/img/video.png'),
      headerLeft2: require('@/assets/img/ia_100000006.png'),
      claimLeft: require('@/assets/img/ia_100000017.png'),
      auctionWork: require('@/assets/img/beetles.png'),
      auctionContentRightCol1: require('@/assets/img/ia_100000020.png'),
      auctionWin: require('@/assets/img/ia_100000021.png'),
      auctionContentLeftCol2: require('@/assets/img/ia_100000022.png'),
      fire: require('@/assets/img/ia_100000028.png'),
      rocket: require('@/assets/img/ia_100000025.png'),
	   rocket2: require('@/assets/img/ia_100000024.png'),
      video: require('@/assets/img/ia_100000019.png'),
      eth: require('@/assets/img/eth.png'),
      bsc: require('@/assets/img/bsc.png'),
      heco: require('@/assets/img/heco.png'),
      xdai: require('@/assets/img/xdai.png'),
      arb: require('@/assets/img/arb.png'),
      polygon: require('@/assets/img/polygon.png'),
      // card item Arrey

      // cardItems: [{heading: 'simply dummy text of the printing 1', paragraph: 'is simply dummy text of the printing and typesettin dummy text of the printing and typesettin dummy text of the printing and typesetting', img: require('@/assets/img/ia_100000030.png')}, {heading: 'simply dummy text of the printing 1', paragraph: 'is simply dummy text of the printing and typesetting', img: require('@/assets/img/ia_100000030.png')}, {heading: 'simply dummy text of the printing 1', paragraph: 'is simpldummy text of the printing and typesettindummy text of the printing and typesettiny dummy text of the printing and typesetting', img: require('@/assets/img/ia_100000030.png')}]

    }
  },
  beforeMount () {
    this.token['0x0000000000000000000000000000000000000000'] = 'ETH'
    // this.token['0x0000000000000000000000000000000000000010'] = 'xx'
  },
  methods: {
    forward (url) {
      window.location.href = url
    },
    /*
    updateFile (arr) {
        const data = JSON.stringify(arr)
        const fs = require('file-system');
        try { fs.writeFileSync('bets.json', data, 'utf-8'); }
        catch(e) { console.log(e) }
    }
    */
    copy(value) {
      navigator.clipboard.writeText(value).then(function() {
        /* clipboard successfully set */
      }, function() {
        /* clipboard write failed */
      });
      this.$bvToast.toast('Successfully copied the contract address.', {
        title: 'Success',
        variant: 'success',
        solid: true,
        toaster: 'b-toaster-bottom-full'
      })
    }
  }
}
</script>

<style scoped>
ul {
  list-style: none;

}

ul li::before {
  content: "\2022";
  color: red;
  display: inline-block; 
  width: 1em;
  margin-left: -1em;
}

button a:hover, button a:active, .min-heading a:hover, min-heading a:active {
  text-decoration:none !important;
}
action-work p {

	text-align: left
}

a {
	color: #fff!important
}
.pointer {
  cursor:pointer;

}
.pointer:hover {
  opacity:0.8;
}
@media screen and (min-width:1400px) {
	.carousel {
		margin-top: -2rem!important
	}
}

@media screen and (min-width:768px) {
		.main-div {
		margin-top: -1rem
	}
	.hidden-lg{
		display: none;
	}
	.carousel {
		margin-top: 6rem
	}
	.button {
		border: 1px solid red;
		border-radius:15px;
		color: #fff;
		font-weight: 200;
		padding: 0.5rem 1rem;
		
		text-align: center;
		 text-transform: capitalize  !important;
		text-decoration: none;
		display: inline-block;
		font-size: 14px;
		margin: 4px 7px
	}
	.button-outlated, .button-outlated2 {
  color: #fff;
  border: 1px solid #fff;
   border-radius:15px !important;
		font-weight: 200;
		
		text-align: center;
		 letter-spacing: 3px;
		 text-transform: capitalize  !important;
		text-decoration: none;
    padding:15px 22px;
		display: inline-block;
		font-size: 14px;
		margin: 4px 7px
}
.button-outlated2 {
  color: red;
  border:1px solid red;
}
	.button:hover {
		opacity: .8;
		text-decoration: none
	}
}

@media screen and (max-width:600px) {
  .nt-3 {
    margin-top:-3rem;
  }
	.video-top {
		margin-top: 5em
	}
	.hidden-sm{
		display: none;
	}
	.breck {
		margin-top: 4em;
	}
	.img-content{
		margin-top: -20%;
	
	}
	.content-card{
		background-color: black;
		border-radius: 20px;
	}
	.action-img{
		margin-top: 200px;
		
	}
	.video-small {
		margin-top:-10% !important;
	}
	.content-video {
		font-size: 1em !important;
		font-family: 'Roboto', serif;
	}
	.content-video-text {
		font-size: 0.9em !important;
		font-family: 'Roboto', serif;
		color:#fff
	}
	.content h2 {
		font-size: 1.2em !important;
		font-family: 'Roboto', serif;
	}
	.content p {
		font-size: 0.9em !important;
		font-family: 'Roboto', serif;
		color:#fff
	}
		.main-div {
		margin-top: -1rem
	}
	.img-size{
		margin: auto;
		width: 250px;
	}
	.polygon {
		margin-top: 10% !important;
		height: 60%;
		width: 60%;
	}
	.shape-up-height-img{
		margin-top: -80%;
	}
	.shape-img {
		background: transparent !important;
		animation: morphs 8s ease-in-out infinite;
		border-radius: 60% 40% 30% 70%/60% 30% 70% 40%;
		height: 163px;
		transition: all 30s ease-in-out;
		width: 163px;
		z-index: 5
	}
	.shape-up-heigh{
		margin-top: -100%;
	}
	.shape-up {
		background: transparent !important;
		animation: morphse 8s ease-in-out infinite;
		border-radius: 60% 40% 30% 70%/60% 30% 70% 40%;
		height: 310px;
		transition: all 30s ease-in-out;
		width: 310px;
		z-index: 5
	}
	@keyframes morphse {
		0% {
			border-radius: 60% 40% 30% 70%/60% 30% 70% 40%;
			background: linear-gradient(45deg, var(--danger ) 0, var(--danger ) 100%)
		}
		50% {
			border-radius: 30% 60% 70% 40%/50% 60% 30% 60%;
			background: linear-gradient(45deg, var(--danger ) 0, var(--danger ) 100%)
		}
		100% {
			border-radius: 60% 40% 30% 70%/60% 30% 70% 40%;
			background: linear-gradient(45deg, var(--danger ) 0, var(--danger ) 100%)
		}
	}
	
	@keyframes morphs {
		0% {
			border-radius: 60% 40% 30% 70%/60% 30% 70% 40%;
			background: linear-gradient(45deg, rgb(0, 7, 6) 0, rgb(0, 7, 6) 100%)
		}
		50% {
			border-radius: 30% 60% 70% 40%/50% 60% 30% 60%;
			background: linear-gradient(45deg,rgb(0, 7, 6) 0, rgb(0, 7, 6) 100%)
		}
		100% {
			border-radius: 60% 40% 30% 70%/60% 30% 70% 40%;
			background: linear-gradient(45deg, rgb(0, 7, 6) 0, rgb(0, 7, 6) 100%)
		}
	}

	.min-heading p {
		font-size: 0.9em !important;
		color: #fff !important;
		font-family: 'Roboto', serif;
	}
	.heading-title {
		font-size: 20px !important;
		font-family: 'Roboto', serif;
	}
	.action h2 {
		margin-top: 20px;
		font-size: 30px;
		color: #fff;
		text-align: center;
		font-weight: 700
	}
	.action p {
		margin-top: 10px;
		font-size: 1.25rem;
		color: #7f7171;
		margin-left: 5%;
		margin-right: 5%;
		text-align: center
	}
	.card-row {
		margin-top: 15%
	}
	.rocket-col {
		margin-top: 60px
	}
	.card-row h1 {
		font-size: 35px;
		margin-left: 10%;
		margin-right: 10%;
		color: #00409e;
		text-align: center;
		font-weight: 700
	}
	.card-row p {
		margin-top: 10px;
		font-size: 20px;
		color: #140707;
		margin-left: 10%;
		margin-right: 10%;
		text-align: start;
		font-weight: 700
	}
	.min-heading {
		margin-top: 0
	}
	.min-heading h1 {
		margin-top: 20px;
		font-size: 1.5rem;
		margin-left: 3%;
		margin-right: 3%;
		text-align: center
	}
	.down-top {
		margin-top: -30em
	}
	.action-work {
		margin-top: -100%
	}
	.action-work h2 {
		padding-left: .5rem;
		padding-right: .5rem;
		font-size: 20px!important;
		font-weight: 700;
		color: #fff !important;
		font-family: 'Roboto', serif;
	}
	.action-work p {
		font-size: 17px;
		color: #7f7171;
		margin-left: 3%;
		margin-right: 5%;
		text-align: start;
		color: #fff !important;
		font-family: 'Roboto', serif;
	}
	.down-top h1 {
		color: #fdfdfd
	}
	.video-modal {
		width: 300px;
		height: 200px
	}
	.down-top h3 {
		text-align: center
	}
	.action-button {
		left: 10%;
		right: 10%;
		margin-bottom: -2.5em
	}
	.circular {
		margin-top: 25em;
		height: 100%;
		width: 100%;
		background-size: cover
	}
	.claim-right-image {
		margin-top: 10em;
		width: 38%;
		float: right
	}
	.image-show {
		margin-bottom: 2;
		right: 0;
		height: 700px;
		width: 900px;
		overflow: hidden;
		background-size: cover;
		background-position: center center;
		background-repeat: no-repeat;
		display: inline-block;
		vertical-align: middle;
		max-width: 100%
	}
	.min-heading p {
		margin-left: 3%;
		margin-right: 3%;
		font-size: 17px;
		text-align: center;
		color: #7f7171
	}
	.videobutton {
		margin-top: -45%;
		margin-left: 30%
	}
	.button {
		border: 1px solid red;
		border-radius:14px;
		color: #fff;
		font-weight: 200;
		padding: 0.5rem 1rem;
		
		text-align: center;
		 text-transform: capitalize  !important;
		text-decoration: none;
		display: inline-block;
		font-size: 14px;
		margin: 4px 7px
	}
	.button-outlated, .button-outlated2 {
  color: #fff;
  border: 1px solid #fff;
   border-radius:15px !important;
		font-weight: 200;
		padding: 15px 22px;
		
		text-align: center;
		 letter-spacing: 3px;
		 text-transform: capitalize  !important;
		text-decoration: none;
		display: inline-block;
		font-size: 14px;
		margin: 4px 7px
}
.button-outlated2 {
  color:red;
  border:1px solid red;
  padding:5px 10px 5px;
}
	.button:hover {
		opacity: .8;
		text-decoration: none
	}
	.block {
		display: block;
		width: 100%;
		border: none;
		background-color: #4caf50;
		padding: 14px 28px;
		font-size: 16px;
		cursor: pointer;
		text-align: center
	}
	.fire-token-top {
		margin-bottom: -120%
	}
	.fire-token {
		margin-bottom: -28%
	}
	.fire {
		margin-bottom: -20%
	}
	.fire-token-down {
		margin-top: 5%;
		margin-bottom: -10%
	}
	.claim-right {
		margin-top: 37em;
		margin-left: 3.4em
	}
	.vert-move {
		-webkit-animation: mover .1s infinite alternate;
		animation: mover .1s infinite alternate
	}
	.vert-move {
		-webkit-animation: mover .1s infinite alternate;
		animation: mover .1s infinite alternate
	}
	@-webkit-keyframes mover {
		0% {
			transform: translateY(0)
		}
		100% {
			transform: translateY(-2px)
		}
	}
	@keyframes mover {
		0% {
			transform: translateY(0)
		}
		100% {
			transform: translateY(-2px)
		}
	}
	@keyframes orbit2 {
		from {
			transform: rotate(0) translateX(50px) rotate(0)
		}
		to {
			transform: rotate(360deg) translateX(50px) rotate(-360deg)
		}
	}
	@-webkit-keyframes orbit1 {
		from {
			-webkit-transform: rotate(0) translateX(70px) rotate(0)
		}
		to {
			-webkit-transform: rotate(360deg) translateX(50px) rotate(-300deg)
		}
	}
	@-moz-keyframes orbit1 {
		from {
			-moz-transform: rotate(0) translateX(70px) rotate(0)
		}
		to {
			-moz-transform: rotate(360deg) translateX(50px) rotate(-300deg)
		}
	}
	@-o-keyframes orbit1 {
		from {
			-o-transform: rotate(0) translateX(70px) rotate(0)
		}
		to {
			-o-transform: rotate(360deg) translateX(50px) rotate(-300deg)
		}
	}
	@keyframes orbit1 {
		from {
			transform: rotate(0) translateX(70px) rotate(0)
		}
		to {
			transform: rotate(360deg) translateX(50px) rotate(-300deg)
		}
	}
	@-webkit-keyframes orbit0 {
		from {
			-webkit-transform: rotate(0) translateX(70px) rotate(0)
		}
		to {
			-webkit-transform: rotate(-360deg) translateX(50px) rotate(360deg)
		}
	}
	@-moz-keyframes orbit0 {
		from {
			-moz-transform: rotate(0) translateX(70px) rotate(0)
		}
		to {
			-moz-transform: rotate(-360deg) translateX(50px) rotate(360deg)
		}
	}
	@-o-keyframes orbit0 {
		from {
			-o-transform: rotate(0) translateX(70px) rotate(0)
		}
		to {
			-o-transform: rotate(-360deg) translateX(50px) rotate(360deg)
		}
	}
	@keyframes orbit0 {
		from {
			transform: rotate(0) translateX(70px) rotate(0)
		}
		to {
			transform: rotate(-360deg) translateX(50px) rotate(-360deg)
		}
	}
	.fire-move {
		z-index: 1;
		-webkit-animation: fire 1s infinite alternate;
		animation: fire 1s infinite alternate
	}
	@-webkit-keyframes fire {
		0% {
			transform: translateY(0)
		}
		100% {
			transform: translateY(-25px)
		}
	}
	@keyframes fire {
		0% {
			transform: translateY(0)
		}
		100% {
			transform: translateY(-25px)
		}
	}
	.shape {
		background: linear-gradient(45deg, var(--primary) 0, var(--secondary) 100%);
		animation: morph 8s ease-in-out infinite;
		border-radius: 60% 40% 30% 70%/60% 30% 70% 40%;
		height: 77px;
		transition: all 1s ease-in-out;
		width: 77px;
		margin-top: -2.7em;
		margin-left: .6em;
		z-index: 5
	}
	@keyframes morph {
		0% {
			border-radius: 60% 40% 30% 70%/60% 30% 70% 40%;
			background: linear-gradient(45deg, var(--primary) 0, var(--secondary) 100%)
		}
		50% {
			border-radius: 30% 60% 70% 40%/50% 60% 30% 60%;
			background: linear-gradient(45deg, var(--third) 0, var(--secondary) 100%)
		}
		100% {
			border-radius: 60% 40% 30% 70%/60% 30% 70% 40%;
			background: linear-gradient(45deg, var(--primary) 0, var(--secondary) 100%)
		}
	}
}

@media screen and (min-width:601px) {
	.my-class {
		display: none;
		background: #000;
		color: #fff
	}
	.content-action h2 {
		text-align: center;
		margin-top: 20px;
		display: block;
		width: 450px;
		color: rgb(255 255 255);
		font-size: 50px;
		line-height: 55px;
		text-shadow: 0 0 20px #002056;
		font-weight: 900!important
	}
	.min-heading {
		margin-top: 40px;
		padding-right: 5%
	}
	.claim-left {
		margin-top: -15%;
		margin-left: -25%
	}
	.card-row {
		margin-top: 5%
	}
	.card-row h1 {
		font-size: 45px;
		margin-left: 10%;
		margin-right: 10%;
		color: #00409e;
		text-align: center;
		font-weight: 700
	}
	.card-row p {
		margin-top: 10px;
		font-size: 1.5rem;
		color: #140707;
		margin-left: 10%;
		margin-right: 10%;
		text-align: start;
		font-weight: 700
	}
	.content-action p {
		margin-top: 10px;
		color: #7f7171;
		text-align: start
	}
	.rocke-img {
		margin-top: -6%;
		margin-left: 18%
	}
	.claim-right-main {
		margin-top: -30%;
		margin-left: 80%
	}
	.min-heading h1 {
		margin-top: 20px;
		font-size: 35px;
		margin-left: 3%;
		margin-right: 3%;
		text-align: center;
		font-weight: 700
	}
	.image-show {
		right: 0;
		height: 100%;
		margin-bottom: 5%;
		width: 100%;
		overflow: hidden;
		background-size: cover;
		background-position: center center;
		background-repeat: no-repeat;
		display: inline-block;
		vertical-align: middle;
		max-width: 100%
	}
	.action-work h2 {
		padding-left: .5rem;
		padding-right: .5rem;
		font-size: 40px!important;
		font-weight: 700
	}
	.action-work p {
		margin-left: 5%;
		margin-right: 5%;
		font-size: 22px;
		color: #7f7171;
		text-align: center
	}
	.min-heading p {
		margin-left: 3%;
		margin-right: 3%;
		font-size: 23px;
		text-align: center;
		color: #7f7171
	}
	.button {
		border: 1px solid red;;
		border-radius:14px;
		color: #fff;
		font-weight: 700;
		padding: 0.5rem 1rem;
		text-align: center;
		text-decoration: none;
		display: inline-block;
		font-size: 14px;
		margin: 4px 2px
	}
	.button:hover {
		opacity: .8;
		text-decoration: none
	}
	.content-action p {
		display: block;
		max-width: 450px;
		position: relative;
		text-shadow: 0 0 20px #001740;
		text-align: center
	}
	.card-section p {
		display: block;
		margin-block-start: 1em;
		margin-block-end: 1em;
		margin-inline-start: 0;
		font-size: 22px;
		color: rgb(47 47 47);
		text-align: center;
		font-weight: 700;
		opacity: .9;
		left: 10%;
		right: 10%
	}
	.down-top {
		margin-top: -35em
	}
	.videobutton {
		margin-top: -50%;
		margin-left: 40%
	}
	@keyframes moveInLeft {
		0% {
			opacity: 0;
			transform: translateX(-100px)
		}
		80% {
			transform: translateX(10px)
		}
		100% {
			opacity: 1;
			transform: translate(0)
		}
	}
	.shape {
		background: linear-gradient(45deg, var(--primary) 0, var(--secondary) 100%);
		animation: morph 8s ease-in-out infinite;
		border-radius: 60% 40% 30% 70%/60% 30% 70% 40%;
		height: 77px;
		transition: all 1s ease-in-out;
		width: 77px;
		margin-top: -2.7em;
		margin-left: .6em;
		z-index: 5
	}
	.card-section h1 {
		margin-top: 2em;
		margin-bottom: 44px;
		font-size: 92px;
		color: rgb(0 64 158)
	}
	.card-section {
		margin-top: -12em
	}
	.video-top {
		margin-top: -15em
	}
	.video-modal {
		width: 400px;
		height: 300px
	}
	.rocket-col {
		margin-bottom: -7em
	}
	.margin-col {
		margin-top: -12%
	}
	.fire-token-top {
		margin-bottom: -52%
	}
	.fire-token {
		margin-bottom: -12%
	}
	.fire {
		margin-bottom: -20%
	}
	.fire-token-down {
		margin-top: 5%;
		margin-bottom: -10%
	}
	.center {
		margin-top: 0;
		display: block;
		margin: auto
	}
	.box-top {
		position: relative;
		top: 50%;
		margin-left: -2.25em;
		animation: circle 3s infinite;
		background: #fecc76;
		clip-path: circle(75%);
		height: 30px;
		width: 30px
	}
	.box {
		position: relative;
		top: 50%;
		margin-left: -2.25em;
		animation: circle 3s infinite;
		background: orange;
		clip-path: circle(75%);
		height: 30px;
		width: 30px
	}
	@keyframes circle {
		0% {
			clip-path: circle(75%)
		}
		50% {
			clip-path: circle(25%)
		}
		100% {
			clip-path: circle(75%)
		}
	}
	.content-border {
		border-left: 10px solid #fecc76
	}
	.circular {
		margin-top: 20%;
		height: 100%;
		margin-bottom: 10%;
		width: 100%;
		background-size: cover
	}
	.claim {
		margin-top: 20%
	}
	.claim-right {
		margin-top: -46em;
		margin-left: 33.4em
	}
	.auction {
		margin-top: 00em;
		background-color: #fff
	}
	.parent {
		position: relative;
		top: 0;
		left: 0;
		margin-bottom: 4em;
		margin-top: -3.4em
	}
	.image1 {
		position: relative;
		left: 0;
		z-index: 1
	}
	.image2 {
		position: absolute;
		top: 70px;
		left: 30px;
		z-index: 2
	}
	.heading h1 {
		font-size: 60px;
		line-height: 69px;
		margin-bottom: 15px;
		letter-spacing: 1px;
		display: block;
		width: 600px;
		justify-content: center;
		color: rgb(0 61 149);
		position: relative;
		letter-spacing: -3px
	}
	.heading p {
		font-size: 1.5rem;
		line-height: 34px;
		margin: 0;
		margin-bottom: 38px;
		text-align: center;
		position: relative;
		color: rgb(103 103 103);
		margin-right: 75px;
		margin-left: 50px;
		top: 10px
	}
	@-webkit-keyframes orbit2 {
		from {
			-webkit-transform: rotate(0) translateX(50px) rotate(0)
		}
		to {
			-webkit-transform: rotate(360deg) translateX(50px) rotate(-360deg)
		}
	}
	@-moz-keyframes orbit2 {
		from {
			-moz-transform: rotate(0) translateX(50px) rotate(0)
		}
		to {
			-moz-transform: rotate(360deg) translateX(50px) rotate(-360deg)
		}
	}
	@-o-keyframes orbit2 {
		from {
			-o-transform: rotate(0) translateX(50px) rotate(0)
		}
		to {
			-o-transform: rotate(360deg) translateX(50px) rotate(-360deg)
		}
	}
	@keyframes orbit2 {
		from {
			transform: rotate(0) translateX(50px) rotate(0)
		}
		to {
			transform: rotate(360deg) translateX(50px) rotate(-360deg)
		}
	}
	@-webkit-keyframes orbit1 {
		from {
			-webkit-transform: rotate(0) translateX(70px) rotate(0)
		}
		to {
			-webkit-transform: rotate(360deg) translateX(50px) rotate(-300deg)
		}
	}
	@-moz-keyframes orbit1 {
		from {
			-moz-transform: rotate(0) translateX(70px) rotate(0)
		}
		to {
			-moz-transform: rotate(360deg) translateX(50px) rotate(-300deg)
		}
	}
	@-o-keyframes orbit1 {
		from {
			-o-transform: rotate(0) translateX(70px) rotate(0)
		}
		to {
			-o-transform: rotate(360deg) translateX(50px) rotate(-300deg)
		}
	}
	@keyframes orbit1 {
		from {
			transform: rotate(0) translateX(70px) rotate(0)
		}
		to {
			transform: rotate(360deg) translateX(50px) rotate(-300deg)
		}
	}
	@-webkit-keyframes orbit0 {
		from {
			-webkit-transform: rotate(0) translateX(70px) rotate(0)
		}
		to {
			-webkit-transform: rotate(-360deg) translateX(50px) rotate(360deg)
		}
	}
	@-moz-keyframes orbit0 {
		from {
			-moz-transform: rotate(0) translateX(70px) rotate(0)
		}
		to {
			-moz-transform: rotate(-360deg) translateX(50px) rotate(360deg)
		}
	}
	@-o-keyframes orbit0 {
		from {
			-o-transform: rotate(0) translateX(70px) rotate(0)
		}
		to {
			-o-transform: rotate(-360deg) translateX(50px) rotate(360deg)
		}
	}
	@keyframes orbit0 {
		from {
			transform: rotate(0) translateX(70px) rotate(0)
		}
		to {
			transform: rotate(-360deg) translateX(50px) rotate(-360deg)
		}
	}
	@keyframes morph {
		0% {
			border-radius: 60% 40% 30% 70%/60% 30% 70% 40%;
			background: linear-gradient(45deg, var(--primary) 0, var(--secondary) 100%)
		}
		50% {
			border-radius: 30% 60% 70% 40%/50% 60% 30% 60%;
			background: linear-gradient(45deg, var(--third) 0, var(--secondary) 100%)
		}
		100% {
			border-radius: 60% 40% 30% 70%/60% 30% 70% 40%;
			background: linear-gradient(45deg, var(--primary) 0, var(--secondary) 100%)
		}
	}
	.vert-move {
		-webkit-animation: mover .1s infinite alternate;
		animation: mover .1s infinite alternate
	}
	.vert-move {
		-webkit-animation: mover .1s infinite alternate;
		animation: mover .1s infinite alternate
	}
	@-webkit-keyframes mover {
		0% {
			transform: translateY(0)
		}
		100% {
			transform: translateY(-2px)
		}
	}
	@keyframes mover {
		0% {
			transform: translateY(0)
		}
		100% {
			transform: translateY(-2px)
		}
	}
	.fire-move {
		z-index: 1;
		-webkit-animation: fire 1s infinite alternate;
		animation: fire 1s infinite alternate
	}
	.fire-move {
		z-index: 1;
		-webkit-animation: fire 1s infinite alternate;
		animation: fire 1s infinite alternate
	}
	@-webkit-keyframes fire {
		0% {
			transform: translateY(0)
		}
		100% {
			transform: translateY(-25px)
		}
	}
	@keyframes fire {
		0% {
			transform: translateY(0)
		}
		100% {
			transform: translateY(-25px)
		}
	}
}
</style>