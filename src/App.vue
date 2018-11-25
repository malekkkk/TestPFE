<template>
    <div class="backgroundColar">
        <buttonsComponent />
        <invitationComponent />

        <onGoingComponent />

        <offerSentComponent />

        <div class="footer">
            <div class="footerItems">
                <p style="color:gray">© 2018 Inter Action Digital.</p>
                <p style="color:gray">all rights are reserved.</p>
            </div>

            <div class="footerItems">
                <p class="grayColar2">Legal notices</p>
                <p class="grayColar2">General Terms and Conditions of Sales</p>
            </div>
            <img class="logo" src="./thePriceHub.png">

            <div class="footerItems">
                <p class="grayColar2">+33 (0)1 73 01 53 23</p>
                <p class="grayColar2">customerssupport@thepricehub.com</p>

            </div>

            <div class="footerItems">
                <p class="grayColar2">Station F</p>
                <p style="color:gray">75013 Paris FRANCE</p>
            </div>

        </div>

    </div>
</template>

<script>
import buttonsComponent from './components/buttonsComponent.vue'
import invitationComponent from './components/invitationComponent.vue'
import onGoingComponent from './components/onGoingComponent.vue'
import offerSentComponent from './components/offerSentComponent.vue'

export default {
  name: 'app',
  components: {
    buttonsComponent,
    invitationComponent,
    offerSentComponent,
    onGoingComponent,
  }
}
</script>

<style>

    .backgroundColar {
        background-color: rgb(242, 241, 246);
        margin-left: -10px;
        margin-right: -10px;
    }
    .footer {
        left: 0;
        bottom: 0;
        width: 100%;
        height: 100px;
        color: white;
        display: -webkit-inline-box;
    }

    .footerItems {
        margin-left: 30px;
        margin-top: 20px;
    }

    .logo {
        width: 140px;
        margin-top: 17px;
        margin-left: 93px;
        margin-right: 69px;
    }

    .grayColar2 {
        color: #808080a8;
    }
   
</style>
