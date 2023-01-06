<template>
  <div id="transaction-main">
    <div class="container">
      <div class="row">
        <div class="col-md-5">
          <div class="transaction-left">
            <h3>
              The amazing NFT art <br />
              of the world here
            </h3>
          </div>
        </div>
        <div class="col-md-7">
          <div class="transaction-right">
            <div class="row">
              <div
                class="col-md-6 transaction-inner-right"
                v-for="transaction in transactions"
                :key="transaction.id"
              >
                <div class="row">
                  <div class="col-md-2">
                    <img :src="transaction.image" alt="image" />
                  </div>
                  <div class="col-md-10">
                    <h5>{{ transaction.name }}</h5>
                    <p>{{ transaction.description }}</p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      transactions: [
        {
          id: 0,
          name: "Fast Transaction",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam etiam viverra tellus imperdiet.",
          image: "/src/assets/img/transaction/card-tick-1.png",
        },
        {
          id: 1,
          name: "Growth Transaction",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam etiam viverra tellus",
          image: "/src/assets/img/transaction/chart-square 2.png",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "../style.scss";

div#transaction-main {
  padding: 100px 0px;
  margin: 50px 0px;
  background: rgb(217 224 236 / 30%);
  .transaction-left {
    h3 {
      font-family: $fontFamily;
      font-weight: $fontBold;
      margin: 0;
      margin-top: 10px;
    }
  }
  .transaction-right {
    p {
      color: #696969;
      font-size: 14px;
      margin: 0;
    }
  }
}
</style>