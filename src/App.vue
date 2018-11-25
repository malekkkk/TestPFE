<template>
    <div class="backgroundColar">
        <div class="topbar">
            <button class="offreSentFilterbutton" v-on:click="offerSentComponentState=true;ongoingComponentState=false;invitationComponentState=false">
                <span class="fontNumber">2</span>
                <br />
                <span>Offers sent</span>
                <br />
                <hr class="hrOfferSent">
            </button>
            <button class="onGoingFRQFilterbutton" v-on:click="ongoingComponentState=true;invitationComponentState=false;offerSentComponentState=false">
                <span class="fontNumber">1</span>
                <br />
                <span>Ongoing RFQ</span>
                <br />
                <hr class="hrOnGoingRFQs">
            </button>
            <button class="invitationFilterbutton" v-on:click="invitationComponentState=true;ongoingComponentState=false;offerSentComponentState=false">
                <span class="fontNumber">1</span>
                <br />
                <span >Invitations</span>
                <br />
                <hr class="hrInvitation">
            </button>
        </div>
        <div>
            <invitationComponent v-if="invitationComponentState===true"></invitationComponent>

            <onGoingComponent v-if="ongoingComponentState===true"></onGoingComponent>

            <offerSentComponent v-if="offerSentComponentState===true"></offerSentComponent>
        </div>
        <div class="footer">
            <div class="footerItems">
                <p style="color:gray">© 2018 Inter Action Digital.</p>
                <p style="color:gray">all rights are reserved.</p>
            </div>

            <div class="footerItems">
                <p class="grayColar2">Legal notices</p>
                <p class="grayColar2">General Terms and Conditions of Sales</p>
            </div>
            <img class="logo" sr44c="./thePriceHub.png">

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
import invitationComponent from './components/invitationComponent.vue'
import onGoingComponent from './components/onGoingComponent.vue'
import offerSentComponent from './components/offerSentComponent.vue'
export default {
        name: 'app',
  components: {
    invitationComponent,
    offerSentComponent,
    onGoingComponent,
        },
   data() {
            return {
                invitationComponentState: true,
                ongoingComponentState: true,
                offerSentComponentState: true
            };
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
    .card {
        flex-direction: column;
        justify-content: center;
        font-family: "Open Sans", sans-serif;
        font-size: 100%;
        box-shadow: 2px 4px 8px 0 rgba(0, 0, 0, 0.2);
        margin: auto;
        text-align: center;
        font-family: arial;
    }

    .hrInvitation {
        width: 50px;
        border-width: 1px;
        border-style: solid;
        border-color: #ff9d00;
    }

    .hrOfferSent {
        width: 50px;
        border-width: 1px;
        border-style: solid;
        border-color: #2fff00;
    }

    .hrOnGoingRFQs {
        width: 50px;
        border-width: 1px;
        border-style: solid;
        border-color: #00b4ff;
    }

    .trait_dessus {
        border-top: 1px solid #000;
        width: 700px;
    }

    .fontNumber {
        font-size: xx-large;
    }

    .offreSentFilterbutton {
        margin-top: 10px;
        margin-right: 20px;
        float: right;
        width: 218px;
        height: 94px;
        background-color: white;
        color: gray;
        border-radius: 1px;
    }

        .offreSentFilterbutton:hover {
            color: #2fff00;
            border-color: #2fff00;
            border-width: 4px;
            border-style: groove;
            border-radius: 10px;
        }

        .offreSentFilterbutton:active {
            color: #2fff00;
            border-color: #2fff00;
            border-width: 4px;
            border-style: groove;
            border-radius: 10px;
        }

        .offreSentFilterbutton:focus {
            color: #2fff00;
            border-color: #2fff00;
            border-width: 4px;
            border-style: groove;
            border-radius: 10px;
        }

    .onGoingFRQFilterbutton {
        margin-top: 10px;
        margin-right: 20px;
        float: right;
        width: 218px;
        height: 94px;
        background-color: white;
        color: gray;
        border-color: white;
        border-radius: 10px;
    }

        .onGoingFRQFilterbutton:hover {
            color: #00b4ff;
            border-color: #00b4ff;
            border-width: 4px;
            border-style: groove;
            border-radius: 10px;
        }

        .onGoingFRQFilterbutton:active {
            color: #00b4ff;
            border-color: #00b4ff;
            border-width: 4px;
            border-style: groove;
            border-radius: 10px;
        }

        .onGoingFRQFilterbutton:focus {
            color: #00b4ff;
            border-color: #00b4ff;
            border-width: 4px;
            border-style: groove;
            border-radius: 10px;
        }

    .invitationFilterbutton {
        margin-top: 10px;
        margin-right: 20px;
        float: right;
        width: 218px;
        height: 94px;
        background-color: white;
        color: gray;
        border-color: white;
        border-radius: 10px;
    }

        .invitationFilterbutton:hover {
            color: #ff9d00;
            border-width: 4px;
            border-style: groove;
            border-color: #ff9d00;
            border-radius: 10px;
        }

        .invitationFilterbutton:active {
            color: #ff9d00;
            border-color: #ff9d00;
            border-width: 4px;
            border-style: groove;
            border-radius: 10px;
        }

        .invitationFilterbutton:focus {
            color: #ff9d00;
            border-color: #ff9d00;
            border-width: 4px;
            border-style: groove;
            border-radius: 10px;
        }

    .topbar {
        background-color: #dfe2e9;
        height: 131px;
        margin-top: -10px;
        margin-left: -10px;
        margin-right: -10px;
    }
</style>
