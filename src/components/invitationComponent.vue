<template type="text/x-template" id="grid-template">


    <div style="margin-left:10px">
        <h5 class="title">Invitation</h5>
        <div class="container">
            <h6 class="left">Company Name / Technology</h6>
            <h6 class="center">N of supplier</h6>
            <h6 class="right">Your status</h6>
        </div>
        <div class="card">
            <div v-for="offer in offers"
                 :key="offer">
                <div class="container" v-if="offer.offerStatus === 'Awaiting for approval'">
                    <span class="companyNameAndTechnology">
                        <span class="companyName">
                            {{offer["companyName"]}}
                        </span>
                        <br />
                        <span class="companyTechnology">
                            {{offer["technology"]}}
                        </span>
                    </span>
                    <span class="numberOfSupplier">
                        {{offer["numSuppliers"]}}
                    </span>
                    <span class="status">
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
        name: "invitationComponent",

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

    .status {
        float: right;
        color: Gray;
        font-size: small;
        margin-top: 25px;
        margin-right: 3%;
    }
    .numberOfSupplier {
        display: inline-block;
        color: Gray;
        font-size: small;
        margin-right: 8%;
        margin-top: 2%;
    }

    .companyTechnology {
        float: left;
        font-size: initial;
    }

    .companyName {
        font-size: inherit;
    }

    .companyNameAndTechnology {
        float: left;
        margin-left: 1%;
        margin-top: 1%;
        color: gray;
    }

    .title {
        margin-bottom: -18px;
    }

    .container {
        width: 100%;
        text-align: center;
    }

    .left {
        float: left;
        color: Gray;
        margin-left: 40px
    }

    .center {
        display: inline-block;
        width: 55px;
        color: Gray;
        margin-left: 7%;
    }

    .right {
        float: right;
        margin-right: 110px;
        color: Gray;
    }

    .card {
        box-shadow: 0 4px 2px 0 rgba(0, 0, 0, 0.2);
        transition: 0.3s;
        width: 96%;
        height: 60px;
        margin-left: 2%;
        background-color: white;
        margin-top: -15px;
        border-style: solid;
        border-color: white;
        border-left-color: orange;
        border-width: 5px;
        border-radius: 5px;
    }

        .card:hover {
            box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
        }
</style>