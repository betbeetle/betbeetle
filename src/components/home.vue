<template>
  <div style="background-color: #23323d !important">
    <!--header Section --> 
    <section>
    <b-row style="background-color: #23323d" class="row justify-content-center">
      <b-col class="parent d-none d-md-block" col md="6" lg="6" xl="6">
        <b-img class="image1" :src="headerLeft1"></b-img>
        <b-img class="image2 fire-move" :src="headerLeft2"></b-img>
      </b-col>
      <b-col class="min-heading" md="6" lg="6" xl="6">
        <b-img
          style="width: 180px; display: block; margin: auto"
          :src="logo"
        ></b-img>
        <h1
          class="mt-10"
          style="display: block;"
        >
          YOUR BET ON A SMART CONTRACT — CRYPTO, SPORTS, POLITICS AND MORE.
        </h1>
        <p>
          Decentralized, instant, no registration. Increase your profits by getting passive income and profit from buy backs and burn through the BTL-Token.
        </p>
        <div></div>
        <b-row class="row justify-content-center">
          <b-col class="row justify-content-center">

            <router-link :to="{ name: 'create' }" style="color:#fff !important;">
            <button
              class="button mt-3 pl-2 pb-2 pt-2 pr-2"
              block
              style="background-color: #d60007 !important"
            >
              Create new bet           
            </button>
            </router-link>   

            <button
              class="button mt-3 pl-2 pb-2 pt-2 pr-2"
              block
              style="background-color: transparent !important"
            >
              <a href="https://betbeetle.com/static/assets/whitepaper.pdf">Whitepaper</a>
            </button>

            

            
          </b-col>
        </b-row>
      </b-col>
    </b-row>
    </section>
    <section>
      <b-container data-aos="fade-up" data-aos-delay="200">
      <div v-if="connected">
        <b-tabs class="mt-5 mb-5" >
          <b-tab v-bind:key="cat" v-for="cat of cats" :title="cat">
            <div class="mt-5" v-if="bets[cat]">
            <div v-bind:key="item.id" v-for="item in bets[cat]" data-aos="zoom-in" data-aos-delay="100">
              <router-link :to="{ name: 'detail', params: { id: item.id }}">
                <div class="grid-item large floatLeft">
                  <span class="token">{{ token[item.tokenAddress] }}</span>
                  <img :src="'https://www.betbeetle.com/static/assets/bets/bet_' + item.id + '.jpg'" @error="$event.target.src = 'https://www.betbeetle.com/static/assets/bets/default.jpg'" :alt="item.title" />
                  <div class="info hide-info">
                    <div class="title">{{ item.title }}</div>
                    <div class="description">{{ item.option0 }} vs. {{ item.option1 }}</div>
                    <div class="date float-right">{{ new Date(parseInt(item.endDate) * 1000).toLocaleDateString() }}, {{ new Date(parseInt(item.endDate) * 1000).toLocaleTimeString() }}</div>
                  </div>
                </div>
                </router-link>
              </div>
            </div>
            <div v-else class="ml-3 mt-4">No open bets found.</div>
          </b-tab>
        </b-tabs>
      </div>
      <div class="mt-5" v-else>
        <h1>Not connected</h1>
          <div class="mt-4 mb-5 textfont">
            <div>Please make sure that your wallet is connected to view all bets.</div>
            <div>
            <a class="btn-get-started scrollto" href="https://metamask.app.link/dapp/www.betbeetle.com">Open in Metamask Browser</a> | <a class="btn-get-started scrollto" href="https://metamask.io/download">Install Metamask</a> | <a href="https://link.trustwallet.com/open_url?coin_id=60&url=https://www.betbeetle.com">Open in Trustwallet</a>
            </div>
          </div>
      </div>
      <!--
      <div class="mt-5" v-else>
        <h2>Install Metamask to view bets</h2>
        <div class="mt-4 mb-5">
          <a :class="buttontext != 'Install Metamask now' ? 'disabled' : ''" @click="updateButton()" class="btn-get-started scrollto" href="https://metamask.app.link/dapp/www.betbeetle.com">Install Metamask</a>
        </div> 
      </div>
      -->
    </b-container>
  </section>

    <!--
    <section>
    <b-container>
      <b-row
        style="margin-top: 6em; border: 3px solid #94d4ff; border-radius: 10px"
      >
        <b-col cols="12" sm="12" md="6" lg="6">
          <p>
            <span style="color: #0d59cc; font-weight: bold; font-size: 20px"
              >Contract:</span
            ><span style="color: #192227; font-size: 18px"
              >1dA01e84F3d4e6716sdsdsd</span
            >
          </p>
        </b-col>

        <b-col cols="12" sm="12" md="3" lg="3" class="row justify-content-end">
          <button
            class="block my-1"
            style="background-color: #006ad4 !important"
          >
            Uniswap info
            <i class="fas fa-external-link-alt" aria-hidden="true"></i>
          </button>
        </b-col>
        <b-col cols="12" sm="12" md="3" lg="3" class="row justify-content-end">
          <button
            class="my-1 block"
            style="background-color: #006ad4 !important"
          >
            Trade Now
          </button>
        </b-col>
      </b-row>
    </b-container>

    
    <b-container style="background-color: #23323d !important">
      <b-row class="my-3">
        <b-col class="auction" style="background-color: #23323d !important">
          <div v-b-modal.modal-sm>
            <b-img :src="auction"></b-img>
            <b-modal hide-footer hide-header id="modal-sm" size="sm" centered>
              <div>
                <b-card>
                  <h2 style="color: #f3222b !important; margin: 10%">
                    www.beet.com
                  </h2>
                </b-card>
              </div>
            </b-modal>
          </div>

          <b-row class="row justify-content-center">
            <b-col class="row justify-content-center">
              <button
                class="button mt-3"
                block
                style="background-color: #ca0007 !important"
              >
                <i class="fas fa-gavel mx-2 large" aria-hidden="true"></i>Learn
                More About Auction
              </button>
            </b-col>
          </b-row>
        </b-col>
      </b-row>
    </b-container>
    </section>
    -->

    <!-- animated Section -->
    <section>
    <div data-aos="fade-up" data-aos-delay="200"
      class="image-show justify-content-center mt-3"
    >
      <b-row>
        <b-col class="claim" data-aos="fade-up" data-aos-delay="200">
          <b-img
            class="claim-left d-none d-lg-block fire-move"
            :src="claimLeft"
          >
          </b-img>
          <b-img
            class="claim-right-image claim-right-main fire-move"
            :src="claimRight"
          >
          </b-img>
        </b-col>
      </b-row>
    </div>
    <div class="down-top" style="padding:1rem !important; background:#4A1B21 !important; padding: 5rem 2rem  !important">
      <b-row>
        <b-col class="d-none d-md-block" cols="4" data-aos="fade-up" data-aos-delay="200"></b-col>
        <b-col cols="8" class="down-top-counter" data-aos="fade-up" data-aos-delay="200">
          <h1>Stake your claim (soon).</h1>
          <p style="color: #ffffff !important">
            Receive 82% of all bets fees in $ETH by staking $BTL.
          </p>
          <b-row class="row justify-content-center">
            <b-col cols="12" sm="12" md="6" lg="6" class="down-top-counter">
              <h2 style="color: #ffffff !important">
                1 000 000 BTL
                <!--
                <VueJsCounter
                  start="4596"
                  end="45496520"
                  duration="2000"
                  thousand=","
                  decimal=","
                ></VueJsCounter>
                -->
              </h2>
              <h2>
                TOTAL SUPPLY
              </h2>
            </b-col>
            <b-col cols="12" sm="12" md="6" lg="6" class="down-top-counter">
              <h2 style="color: #ffffff !important">
                0 BTL
                <!--
                <VueJsCounter
                  start="4596"
                  end="1549652"
                  duration="2000"
                  thousand=","
                  decimal=","
                ></VueJsCounter>
                -->
              </h2>
              <h2>
                TOTAL STAKE
              </h2>
            </b-col>
          </b-row>
          <b-row class="row justify-content-center">
            
          </b-row>
        </b-col>
        <b-col cols="2" class="d-none d-md-block" data-aos="fade-up" data-aos-delay="200"> </b-col>
       
        <b-col data-aos="fade-up" data-aos-delay="200"
          cols="10"
          md="8"
          lg="8"
          sm="8"
          class="action-button row justify-content-center"
        >
          <!--
          <button
            class="button mt-3"
            block
            style="background-color: #ca0007 !important"
          >
            Stake now<br />(soon)
          </button>
        -->
        </b-col>
      </b-row>
    </div>
    </section>

    <!-- section video @@ card-->
    <section data-aos="fade-up" data-aos-delay="200">
    <div
      class="circular justify-content-center"
    >
      <b-row class="video-top">
        <b-col cols="12" md="7" lg="7" class="action-work">
          <h1 style="margin-left: 2em; margin-top:2rem; color: #fff">
            How does Betbeetle work?
          </h1>
          <p>
            Learn more on how you create new bets, participate in existing bets and level up to maximize your betting profits.
          </p>
          <p>
          <button
            class="button mt-3"
            block
            style="background-color: #ca0007 !important"
            @click="forward('https://www.medium.com/betbeetle')"
          >
            Read more
          </button>
          </p>
        </b-col>
        <b-col cols="12" md="5" lg="5" class="video-circle">
          <b-row>
            <b-col cols="12">
              <b-img :src="video"> </b-img>
            </b-col>
            <b-col cols="12" class="videobutton">
              <div class="shape" v-b-modal.modal-center>
                <b-img
                  :src="videoButton"
                  style="width: 68px"
                  rounded="circle"
                ></b-img>
              </div>
            </b-col>
          </b-row>
        </b-col>
      </b-row>
      <b-img :src="auctionWork"></b-img>
      <b-container>
        <!-- Grid column -->

        <b-modal hide-footer hide-header id="modal-center" centered>
          <div class="video-modal">
            <iframe
              style="width: 460px; height: 300px"
              src="https://www.youtube.com/embed/A3PDXmYoF5U"
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
          <b-img class="rocke-img" :src="rocket"> </b-img>
        </b-col>
        <b-col md="5" lg="5" cols="" class="d-none d-md-block"> </b-col>
      </b-row>

      <b-row class="row justify-content-center">
        <b-col cols="12" md="6" sm="6" lg="6" class="content-action action">
          <b-img style="" :src="auctionContentRightCol1"> </b-img>
          <h1>Join the $BTL family</h1>
          <p>
            Install Metamask or any other Ethereum wallet and trade your ETH for Betbeetle ($BTL) tokens.
          </p>
          <p>
          <button
            class="button mt-3"
            block
            style="background-color: rgb(214, 0, 7) !important"
          >
            Buy $BID (soon)
          </button>
          </p>
        </b-col>
        <b-col md="1" sm="1" lg="1" class="content-border d-none d-md-block">
          <div class="box-top"></div>
        </b-col>

        <b-col cols="12" md="5" sm="5" lg="5" class="content-action action">
        </b-col>
      </b-row>
      <b-row class="row justify-content-center">
        <b-col cols="12" md="6" lg="6" class="content-action action">
        </b-col>
        <b-col lg="1" sm="1" md="1" class="content-border d-none d-md-block">
          <div class="box"></div>
        </b-col>
        <b-col cols="12" sm="5" md="5" lg="5" class="content-action action">
          <b-img style="" :src="auctionContentLeftCol2"> </b-img>
          <h1>82% reward for $BTL staking</h1>
          <p>
            82% of all fees are rewarded to $BTL stakers in ETH. 10% of the fees are used for executing the monthly buy back and burn.
          </p>
          <p>
          <button
            class="button mt-3"
            block
            style="background-color: #ca0007 !important"
          >
            Stake now<br />(soon)
          </button>
          </p>
        </b-col>
      </b-row>
      <b-row class="row justify-content-center">
        <b-col cols="12" md="6" sm="6" lg="6" class="content-action action">
          <b-img style="" :src="auctionWin"> </b-img>
          <h1>Start winning</h1>
          <p>
            Create bets or participate in existing bets of your friends and other community members. Make new crypto friends in our telegram group.
          </p>
          <p>
          <button
            class="button mt-3"
            @click="forward('https://t.me/betbeetle')"
            block
            style="background-color: rgb(214, 0, 7) !important; "
          >
            Join our telegram<br />group
          </button>
          </p>
        </b-col>
        <b-col md="1" sm="1" lg="1" class="content-border d-none d-md-block">
          <div class="box-top"></div>
        </b-col>

        <b-col cols="12" md="5" sm="5" lg="5" class="content-action action">
        </b-col>
      </b-row>
      <b-row align-v="center margin-col">
        <b-col class="fire" cols="12" sm="12" md="12" lg="12" style="margin-top: 3rem !important;">
          <b-img center class="fire-move" :src="fire"> </b-img>
        </b-col>
        <b-col class="fire-token-down" cols="12" sm="12" md="12" lg="12" style="margin-top: 5rem !important;">
          <b-img center :src="tokensBurned"> </b-img>
        </b-col>
      </b-row>
    </div>
    </section>

    <!--section footer && card -->
    
    <!--
    <section>
    <b-container>
      <div align="center">
        <b-row class="card-row">
          <b-col cols="12">
            <h1>Tokenomics</h1>

            <p>
              The DefiBids ($BID) smart contracts and auction protocols are
              quite complex but the underlying concepts that drive our token are
              relatively simple. Here is a brief overview of our PHASE 1
              tokenomics:
            </p>
          </b-col>

          <b-col
            cols="12"
            class="text-center"
            v-for="(item, index) in cardItems"
            :key="index.item"
          >
            <b-card class="service-card">
              <div
                @mouseover="mouseover(index)"
                @mouseout="mouseover(index)"
                class="nHover-background"
                :class="
                  hoverValue == true && numbeCheck == index
                    ? 'hover-background'
                    : 'nHover-background'
                "
              >
                <b-row
                  style="
                    border-style: solid;
                    border-color: #0144a5;
                    border-radius: 20px;
                  "
                >
                  <b-col
                    cols="12"
                    sm="3"
                    md="2"
                    lg="2"
                    style="margin-top: 2.5em"
                  >
                    <span class="dot">
                      <b-img
                        :class="
                          hoverValue == true && numbeCheck == index
                            ? 'curcular-component-hover'
                            : 'curcular-component-nHover'
                        "
                        :src="curcularComponent"
                      ></b-img>
                      <div class="shape">
                        <b-img :src="item.img"></b-img>
                      </div>
                    </span>
                  </b-col>
                  <b-col
                    cols="12"
                    sm="9"
                    md="8"
                    lg="8"
                    class="bottom-card-section"
                  >
                    <h2>{{ item.heading }}</h2>
                    <p>{{ item.paragraph }}</p>
                  </b-col>
                </b-row>
              </div>
            </b-card>
          </b-col>
        </b-row>
      </div>
    </b-container>
    </section>
    -->
  </div>
</template>

<script>
// import web3 from '../contracts/web3'
import BetContract from '@/contracts/auctionBoxInstance'
import VueJsCounter from 'vue-js-counter'
//
// Wallet Connect
/*
https://docs.walletconnect.org/quick-start/dapps/client

import WalletConnectProvider from "@walletconnect/web3-provider";

//  Create WalletConnect Provider
const provider = new WalletConnectProvider({
  infuraId: "fe0e4d2c3e86450692da89ef38195d1c",
});

//  Enable session (triggers QR Code modal)
*/

export default {
  components: {
    VueJsCounter
  },
  name: 'home',
  data () {
    return {
      showModal: false,
      numbeCheck: 0,
      amount: 0,
      hoverValue: true,
      noMetamask: false,
      noMetamaskDesktop: false,
      connected: false,
      buttontext: 'Install Metamask now',
      publicPath: process.env.BASE_URL,
      cssProps: {
      },
      bets: {},
      token: [],
      cats: [],
      // image import from assets and reaname there
      logo: require('@/assets/img/beetlemoney.gif'),
      headerLeft1: require('@/assets/img/ia_100000036.png'),
      videoButton: require('@/assets/img/video.png'),
      headerLeft2: require('@/assets/img/ia_100000006.png'),
      auction: require('@/assets/img/ia_100000008.png'),
      claimLeft: require('@/assets/img/ia_100000017.png'),
      claimRight: require('@/assets/img/ia_100000009.png'),
      auctionWork: require('@/assets/img/defibids_how-top-cover.png'),
      auctionContentRightCol1: require('@/assets/img/ia_100000020.png'),
      auctionWin: require('@/assets/img/ia_100000021.png'),
      auctionContentLeftCol2: require('@/assets/img/ia_100000022.png'),
      auctionContentRightCol2: require('@/assets/img/ia_100000023.png'),
      auctionContentLeftCol3: require('@/assets/img/ia_100000024.png'),
      tokensBurned: require('@/assets/img/ia_100000029.png'),
      fire: require('@/assets/img/ia_100000028.png'),
      rocket: require('@/assets/img/ia_100000025.png'),
      video: require('@/assets/img/ia_100000019.png'),
      curcularComponent: require('@/assets/img/ia_100000010.png'),
      cardComponent: require('@/assets/img/ia_100000030.png'),
      // card item Arrey

      cardItems: [{heading: 'simply dummy text of the printing 1', paragraph: 'is simply dummy text of the printing and typesettin dummy text of the printing and typesettin dummy text of the printing and typesetting', img: require('@/assets/img/ia_100000030.png')}, {heading: 'simply dummy text of the printing 1', paragraph: 'is simply dummy text of the printing and typesetting', img: require('@/assets/img/ia_100000030.png')}, {heading: 'simply dummy text of the printing 1', paragraph: 'is simpldummy text of the printing and typesettindummy text of the printing and typesettiny dummy text of the printing and typesetting', img: require('@/assets/img/ia_100000030.png')}]

    }
  },
  beforeMount () {
    this.token['0x0000000000000000000000000000000000000000'] = 'ETH'
    // this.token['0x0000000000000000000000000000000000000010'] = 'xx'
    this.connected = this.$store.getters.connected
    if (this.connected) {
      this.getPositivesBets()
    } /* else {
      let isMobile = window.matchMedia('only screen and (max-width: 760px)').matches
      if (isMobile) {
        this.noMetamask = true
      } else {
        this.noMetamaskDesktop = true
      }
    } */

    this.cats = ['Crypto', 'Sports', 'Politics', 'Other']
  },
  methods: {
    forward (url) {
      window.location.href = url
    },
    getPositivesBets () {
      BetContract.methods
      .getPositivesBets(
        0,
        10,
      )
      .call()
      .then((bets) => {
        if (bets) {
          this.bets = bets[0]
          this.bets = this.bets.reduce(function (r, a) {
            r[a[3]] = r[a[3]] || []
            r[a[3]].push(a)
            return r
          }, Object.create(null))

          // this.updateFile(this.bets)

          // set the amount of bets
          this.amount = bets[0].length
        }
      })
    }
    /*
    updateFile (arr) {
        const data = JSON.stringify(arr)
        const fs = require('file-system');
        try { fs.writeFileSync('bets.json', data, 'utf-8'); }
        catch(e) { console.log(e) }
    }
    */
  }
}
</script>

<style>
@import "../assets/styles/startPage.css";
#isBid, #isFin {
  height: 32px;
  margin-top: 16px;
  margin-left: 8px;
}

.grid-container {
  width: 100%;
  max-width: 1280px;
  margin: 0 auto;
  height: auto;
  overflow: hidden;
}

.textfont {
  font-size:1.5rem !important;
}

.floatLeft {
  float: left;
}

.grid-item {
  position: relative;
  overflow: hidden;
  margin: 1.5%;
  height: 0px;
  border:2px solid #4A1B21 !important;
}

.grid-item:hover {
  transform: scale(0.97);
  cursor: pointer;
}

.grid-item:active {
  transform: scale(0.93);
  cursor: pointer;
}

.large {
  width: 30%;
  padding-bottom: 39.55%;
}

.grid-item img {
  overflow: hidden;
  width: 105%;
}

.grid-item .info {
  overflow: hidden;
  position: absolute;
  background-color: #4A1B21 !important;
  bottom: 0;
  height: auto;
  left: 0;
  width: 100%;
  font-size: 100%;
  transition: all 0.25s ease-in-out;
}

.grid-item .show-info {
  height: 100%;
}

.grid-item .hide-info {
  padding: 0.75rem;
  height: 40%;
  max-height: 100px;
}

.grid-item .token {
    top: 2%;
    right: 2%;
    border-radius: 2rem;
    background: #2A3C4A !important;;
    padding: 0.5rem 1rem;
    color: #fff;
    position: absolute;
}

.grid-item .title {
  color:#fff !important;;
  font-weight:600;
  margin-top: 5px;
  font-size: 15px;
  padding: 1%;
}

.grid-item .date {
  padding: 3%;
  padding-top: 5px;
  font-size: 13px;
}

.grid-item .description {
  font-size: 13px;
  padding: 1%;
}

@media all and (max-width:680px) {
  .large {
    width: 90%;
    padding-bottom: 49.3%;
    margin-bottom: 1%;
  }
}
</style>
