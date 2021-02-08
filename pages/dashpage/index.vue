<template>
  <div class="container">
    <div class="section">
      <header>User Info</header>
      <div class="row">
        <label> UserID </label>
        <div class="column">
          <output type="label" name="UserID">{{ UserID }}</output>
        </div>
      </div>
      <div class="row">
        <label> Full name </label>
        <div class="column">
          <output type="label" name="Fullname">{{ Fullname }}</output>
        </div>
      </div>
      <div class="row">
        <label> Username </label>
        <div class="column">
          <output type="label" name="Username">{{ Username }}</output>
        </div>
      </div>
      <div class="row">
        <label> Email Address: </label>
        <div class="column">
          <output type="label" name="EmailAddress">{{ EmailAddress }}</output>
        </div>
      </div>
      <div class="row">
        <label> Phone Number: </label>
        <div class="column">
          <output type="label" name="PhoneNumber">{{ PhoneNumber }}</output>
        </div>
      </div>
      <div class="next-line">
        <div class="row">
          <label> Registration Date: </label>
          <div class="column">
            <output type="label" name="RegistrationDate">{{
              RegistrationDate
            }}</output>
          </div>
        </div>
      </div>
      <div class="row">
        <label> Number of Contests won</label>
        <div class="column">
          <output type="label" name="NumberofContestsWon">{{
            NumberofContestsWon
          }}</output>
        </div>
      </div>
      <div class="row">
        <label> Number of Contests Lost</label>
        <div class="column">
          <output type="label" name="NumberofContestsLost">{{
            NumberofContestsLost
          }}</output>
        </div>
      </div>
    </div>
    <div class="section">
      <header>Recent Contest Info</header>
      <div class="row">
        <label> Contests Name </label>
        <div class="column">
          <output type="label" name="ContestName">{{ ContestName }}</output>
        </div>
      </div>
      <div class="row">
        <label> Start date </label>
        <div class="column">
          <output type="label" name="StartDate">{{ StartDate }}</output>
        </div>
      </div>
      <div class="row">
        <label> Entry Cost </label>
        <div class="column">
          <output type="label" name="EntryCost">{{ EntryCost }}</output>
        </div>
      </div>
      <div class="row">
        <label> Total Price </label>
        <div class="column">
          <output type="label" name="TotalPrice">{{ TotalPrice }}</output>
        </div>
      </div>
      <div class="row">
        <label> Status </label>
        <div class="column">
          <output type="label" name="Status">{{ Status }}</output>
        </div>
      </div>
    </div>
    <div class="section">
      <header>Transaction History</header>
      <br /><br /><br />
      <div class="row">
        <label> Transaction </label>
        <div class="column">
          <output type="label" name="Fund Wallet">Fund Wallet</output>
        </div>
        <div class="column">
          <output type="label" name="Coin Purchase">Coin Purchase</output>
        </div>
      </div>
      <div class="row">
        <label> Amount </label>
        <div class="column">
          <output type="label" name="FundWalletAmount">{{
            FundWalletAmount
          }}</output>
        </div>
        <div class="column">
          <output type="label" name="CoinPurchaseAmount">{{
            CoinPurchaseAmount
          }}</output>
        </div>
      </div>
      <div class="row">
        <label> Date </label>
        <div class="column">
          <output type="label" name="FundWalletDate">{{
            FundWalletDate
          }}</output>
        </div>
        <div class="column">
          <output type="label" name="CoinPurchaseDate">{{
            CoinPurchaseDate
          }}</output>
        </div>
      </div>
      <div class="row">
        <label> Cost </label>
        <div class="column">
          <output type="label" name="FundWalletCost">{{
            FundWalletCost
          }}</output>
        </div>
        <div class="column">
          <output type="label" name="CoinPurchaseCost">{{
            CoinPurchaseCost
          }}</output>
        </div>
      </div>
    </div>
  </div>
</template>


<style>
@import url("https://fonts.googleapis.com/css2?family=Josefin+Sans&display=swap"); /*font import*/
* {
  margin: 0;
  padding: o;
  list-style: none;
  text-decoration: none;
  font-family: "Josefin Sans", sans-serif;
}
.container {
  width: 1200px;
  justify-content: space-between;
  font-size: 12px;
  margin: 70px;
  empty-cells: show;
}
.section {
  display: flex;
  border: 1px solid #ccc;
}
.container div {
  padding: 10px;
  margin: 20px;
}
header {
  align-items: flex-end;
  font-size: 13px;
  margin-bottom: 20px;
  display: inline;
  color: rgba(245, 180, 39, 0.808);
  font-weight: bold;
}
.row {
  width: 20%;
  align-content: flex-start;
}
.column {
  font-weight: bold;
}

.next-line {
  width: 100%;
  align-content: center;
}
</style>

<!--<script>
const App = new Vue({
  el: "#app",
  data: {
    form: {
      UserID: null,
      Fullname: null,
      Username: null,
      EmailAddress: null,
      PhoneNumber: null,
      RegistrationDate: null,
      NumberofContestsWon: null,
      NumberofContestsLost: null,
      ContestName: null,
      StartDate: null,
      EntryCost: null,
      TotalPrice: null,
      Status: null,
      FundWalletAmount: null,
      FundWalletDate: null,
      FundWalletCost: null,
      CoinPurchaseAmount: null,
      CoinPurchaseDate: null,
      CoinPurchaseCost: null,
    },
  },
});
</script>-->