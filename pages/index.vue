<template>
  <div>
    <b-row class="onboarding">
      <b-col md="4" class="m-0 p-0">
        <OnBoardingLeft />
      </b-col>
      <b-col md="8" class="m-0 p-0">
        <OnBoardingRight />
      </b-col>
    </b-row>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss">
.onboarding {
  height: 100%;
  min-height: 100vh;
  margin: 0;
  .text-gray {
    color: #a7a6a6;
  }
  .text-orange {
    color: #ffca00;
  }
  .text-blue {
    color: #4982ff;
  }
  .f-10 {
    font-size: 10px;
  }
  .f-12 {
    font-size: 12px;
  }
  .f-14 {
    font-size: 14px;
  }
  .f-16 {
    font-size: 16px;
  }
}
</style>
