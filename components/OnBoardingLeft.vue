<template>
    <div class="onboarding-left">
        <b-row class="onboarding-logo">
            <b-img src="~/assets/logo.png" width="50" class="ml-3 mb-3" fluid alt="quote-icon"></b-img>
        </b-row>
        <div class="my-5 py-3 trial">
          <div class="pt-2 d-flex justify-content-between">
            <h5 class="trial-text">
              Trial &amp; Pricing
            </h5>
            <span class="">
              <b-img src="~/assets/right.svg" fluid alt="quote-icon"></b-img>
            </span>
          </div>
          <div class="text-gray">
            <h5 class="py-3">Payment Method</h5>
            <span class="space">- - - - - -</span>
            <h6 class="get-started mt-3 mb-5">Get started...</h6>
          </div>
        </div>
        <div class="my-5">
          <blockquote class="blockquote text-left">
          <p class="mb-0 text-gray">
            Success is not final; failure is not fatal; it is the courage to continue that counts
          </p>
          <span class="quote-icon">
            <b-img src="~/assets/quote.svg" fluid alt="quote-icon"></b-img>
          </span>
          <footer class="blockquote-footer">Winston Churchill</footer>
        </blockquote>
        </div>
    </div>
</template>
<style lang="scss">
  .onboarding-left {
    background: #222021;
    color: #ffffff;
    height: 100%;
    padding: 90px;
    .trial {
      position: relative;
      &:before {
        content: '';
        height: 25%;
        width: 5px;
        position: absolute;
        left: -90px;
        top: 0;
        background-color: #ffca00;
      }
    }
    .space {
      color: #ffca00;
    }
    .blockquote {
      border: 1px solid #545353;
      border-radius: 20px;
      padding: 35px 45px 35px 65px;
      font-size: 16px;
      position: relative;
      p {
        z-index: 1;
      }
      .quote-icon {
        position: absolute;
        left: -37px;
        top: 28%;
        padding: 10px 0;
        background: #222021;
        transform: rotate(180deg); 
      }
      .blockquote-footer {
        color: #f9f9f9;
        padding: 10px 0;
      }
    }
  }
</style>