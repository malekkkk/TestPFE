<template>
  <div class="topbar" >
<button class="filterbutton">
                Offers sent
            </button><button class="filterbutton">
                Ongoing RFQ
            </button><button class="filterbutton">
                Invitations
            </button>  </div>
</template>

<script>
    import Data from "./../data.json";

export default {
  
  template: "#grid-template",

  data() {
    return {
      offers: Data.offers
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.card {
  flex-direction: column;
  justify-content: center;
  font-family: "Open Sans", sans-serif;
  font-size: 100%;
  box-shadow: 2px 4px 8px 0 rgba(0, 0, 0, 0.2);
  max-width: 350px;
  margin: auto;
  text-align: center;
  font-family: arial;
}
    .filterbutton {
        margin-top: 18px;
        margin-right: 20px;
        float: right;
        width: 160px;
        height: 90px;
        background-color: white;
        color: gray;
    }
    .filterbutton:hover{
        color:red;
    }
    .topbar {
        background-color: #dfe2e9;
        height: 131px;
        margin-top: -10px;
        margin-left: -10px;
        margin-right: -10px;
    }
</style>
