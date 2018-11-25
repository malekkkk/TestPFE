<template type="text/x-template" id="grid-template">
    <div style="margin-left:10px">
        <h5 class="title">Ongoing RFQs </h5>
        <div class="container">
            <h6 class="left">Company Name / Technology</h6>
            <h6 class="centerOfferAmount">Offer amount</h6>
            <h6 class="centerNombreOfSupplier">N of supplier</h6>
            <h6 class="right">Your status</h6>
        </div>
        <div class="onGoingCard"
             v-for="offer in offers"
             :key="offer">
            <div class="onGoingContainer" v-if="offer.offerStatus === 'Make an offer'">
                <span class="onGoingCompanyNameAndTechnology">
                    <span class="companyName">{{offer["companyName"]}}</span>
                    <br />
                    <span class="companyTechnology">{{offer["technology"]}}</span>
                </span>
                <span class="onGoingOfferAmount">
                    {{offer["offerAmount"]}}
                </span>
                <span class="onGoingNumberOfSuppliers">
                    {{offer["numSuppliers"]}}
                </span>
                <span class="onGoingStatus">
                    {{offer["offerStatus"]}}
                </span>
            </div>
        </div>
    </div>
</template>

<script>
    import Data from "./../data.json";

    export default {
        name: "onGoingComponent",

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

    .onGoingOfferAmount {
        margin-left: -40px;
        margin-right: 90px;
        color: Gray;
        font-size: small;
    }

    .onGoingStatus {
        float: right;
        color: Gray;
        font-size: small;
        margin-top: 15px;
        margin-right: 77px;
    }

    .onGoingNumberOfSuppliers {
        margin-right: 200px;
        margin-left: -15px;
        color: Gray;
        font-size: small;
        display: inline-block;
        margin-top: 15px;
    }

    .companyTechnology {
        float: left;
        font-size: initial;
    }

    .companyName {
        font-size: inherit;
    }

    .onGoingCompanyNameAndTechnology {
        float: left;
        margin-left: 27px;
        color: gray;
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

    .onGoingCard {
        box-shadow: 0 4px 2px 0 rgba(0, 0, 0, 0.2); 
        transition: 0.3s;
        width: 96%;
        height: 28px;
        margin-left: 2%;
        background-color: white;
        margin-top: -15px;
    }

        .onGoingCard:hover {
            box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
        }
</style>