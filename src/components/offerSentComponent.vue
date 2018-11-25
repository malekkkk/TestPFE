<template type="text/x-template" id="grid-template">

    <div style="margin-left:10px">
        <br />
        <h5>Offer Sent</h5>
        <div class="offreSentHeadercontainer">
            <h6 class="left">Company Name / Technology</h6>
            <h6 class="centerOfferAmount">Offer amount</h6>
            <h6 class="centerNombreOfSupplier">N of supplier</h6>
            <h6 class="right">Your status</h6>
        </div>

        <div v-for="offer in offers"
             :key="offer">
            <div class="onGoingContainer" v-if="offer.offerStatus=== 'Waiting for verification'">
                <div class="offreSentCard">
                    <span class="offreSentCompanyNameAndTechnology">
                        <span class="companyName">{{offer["companyName"]}}</span>
                        <br />
                        <span class="companyTechnology">{{offer["technology"]}}</span>
                    </span>
                    <span class="offreSentOfferAmount">
                        {{offer["offerAmount"]}}
                    </span>
                    <span class="offreSentNumberOfSuppliers">
                        {{offer["numSuppliers"]}}
                    </span>
                    <span class="offreSentStatus">
                        {{offer["offerStatus"]}}
                    </span>
                </div>
            </div>
        </div>
    </div>


</template>

<script>
    import Data from "./../data.json";

    export default {
        name: "offerSentComponent",

        data() {
            return {
                offers: Data.offers,
                columns: [
                    "Company - Name / Technology",
                    "N° of suppliers",
                    "Offer Amount",
                    "Your Status"
                ]
            };
        }
    };
</script>

<style>
    .offreSentOfferAmount {
        margin-left: 140px;
        margin-right: 90px;
        color: Gray;
        font-size: small;
    }

    .offreSentHeadercontainer {
        width: 100%;
        text-align: center;
        margin-top: -40px;
    }

    .offreSentStatus {
        float: right;
        color: Gray;
        font-size: small;
        margin-right: 7%;
        margin-top: 2%;
    }

    .offreSentNumberOfSuppliers {
        margin-left: -50px;
        margin-right: 224px;
        color: Gray;
        font-size: small;
        display: inline-block;
        margin-top: 15px;
        text-align: center;
    }

    .companyTechnology {
        float: left;
        font-size: initial;
    }

    .companyName {
        font-size: inherit;
    }

    .offreSentCompanyNameAndTechnology {
        float: left;
        margin-left: 27px;
        color: gray;
        margin-right: 90px;
        margin-top: 10px;
    }

    .title {
        margin-bottom: -18px;
    }

    .onGoingContainer {
        width: 100%;
        text-align: center;
    }

    .left {
        float: left;
        color: Gray;
        margin-left: 40px
    }

    .centerOfferAmount {
        display: inline-block;
        color: Gray;
    }

    .centerNombreOfSupplier {
        margin-left: 40px;
        display: inline-block;
        color: Gray;
        width: 40px;
    }

    .right {
        float: right;
        margin-right: 110px;
        color: Gray;
    }

    .offreSentCard {
        box-shadow: 0 4px 2px 0 rgba(0, 0, 0, 0.2);
        transition: 0.3s;
        width: 96%;
        height: 60px;
        margin-left: 2%;
        background-color: white;
        margin-bottom: 30px;
        margin-top: -11px;
        border-style: solid;
        border-color: white;
        border-left-color: #2fff00;
        border-width: 5px;
        border-radius: 5px;
    }

        .offreSentCard:hover {
            box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
        }
</style>