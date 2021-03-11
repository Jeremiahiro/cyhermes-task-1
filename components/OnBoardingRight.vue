<template>
    <div class="onboarding-right">
      <b-row>
        <b-col md="8">
          <p class="m-0 p-0 text-uppercase font-weight-bold text-gray">Hey, Terry</p>
          <h4 class="font-weight-bold">Start your <i class="text-orange">30 days</i> Trial</h4>
          <span class="text-gray f-12">
            Select your preferred packgage below
          </span>
        </b-col>
        <b-col md="4">
          <p class="m-0 p-0 text-uppercase text-blue"><b>NGN</b></p>
          <h4 class="m-0 p-0 text-blue"><b>1,999,999</b></h4>
          <p class="m-0 p-0 text-gray"><b>Total</b> <span class="text-uppercase f-12">(excludes vat)</span></p>
        </b-col>
      </b-row>
      <b-row class="mt-5">
        <b-col align-self="end">
          <b-card
              class="start-card"
              no-title
            >
              <b-card-text>
                <div>
                  <p class="m-0 p-0 text-orange f-12">Starts From</p>
                  <p class="m-0 p-0 text-gray f-12 text-uppercase">NGN</p>
                  <h5 class="m-0 p-0"><b>5,999,999.99</b></h5>
                  <p class="m-0 p-0 text-muted f-12">per annum</p>
                </div>
                <div class="mt-3">
                  <h4>Premium</h4>
                  <p class="m-0 p-0">100 Users <span>.</span> All Modules</p>
                </div>
              </b-card-text>
            </b-card>
        </b-col>
        <b-col>
          <b-card class="basic-card" >
            <b-card-text>
              <span class="check">
                <b-img src="~/assets/check.svg" fluid alt="icon"></b-img>
              </span>
              <div>
                <h4 class="text-blue"><b>Basic</b></h4>
                <p class="m-0 p-0 text-gray">
                  <b>30 days trials</b> on our premium app features and features
                </p>
              </div>
              <div class="mt-4">
                <h6 class="text-uppercase text-gray">Includes
                  <span class="text-blue">- - - - - - - - - - - - -</span>
                </h6>
                <div class="text-gray ">
                  <p class="m-0 p-0">- 25 Users</p>
                  <p class="m-0 p-0">- All modules &amp; features</p>
                  <p class="m-0 p-0">- Unlimited commitees</p>
                  <p class="m-0 p-0">- Unlimited roles creation</p>
                </div>
              </div>
            </b-card-text>
          </b-card>
        </b-col>
      </b-row>
      <div class="mt-3 text-gray f-14">
        <h5 class="m-0 p-0">Add more users</h5>
        <p class="m-0 p-0"><b>NGN 99,999</b> per user</p>
      </div>
      <div class="my-3">
        <div class="d-flex justify-content-between">
          <small><b>0</b></small>
          <small class="text-blue"><b>{{ value }}</b></small>
          <small><b>>1000</b></small>
        </div>
        <b-form-input id="fee-range" name="fee-range" v-model="value" type="range" min="0" max="1000" step="100"></b-form-input>
      </div>
      <b-container class="mb-5 module">
        <div class="module-header">
          All Modules
        </div>
        <b-row cols="3">
          <b-col
            v-for="(item, i) in modules"
            :key="i"
            class="p-3 mb-2 f-14 text-gray module-item"
            :class="{active: i === 0 }"
          >
            <b-row>
              <b-col md="3">
                <b-img :src="item.img" fluid :alt="item.description"></b-img>
              </b-col>
              <b-col md="6">{{ item.description }}</b-col>
              <b-col md=3>
                <span v-show="i === 0">
                  <b-img class="mt-3" src="~/assets/warning.svg" fluid alt="icon"></b-img>
                </span>
              </b-col>
            </b-row>
          </b-col>
        </b-row>
      </b-container>
      <div class="d-flex justify-content-between">
        <b-button variant="default" class="text-danger">Go Back</b-button>
        <b-button variant="warning" class="font-weight-bold px-4">Continue</b-button>
      </div>
    </div>
</template>

<script>
  export default {
    data() {
      return {
        value: '100',
        modules: [
          {
            img: 'https://res.cloudinary.com/iro/image/upload/v1615454283/tweb/category/parliament.svg',
            description: 'Governance Portal'
          },
          { 
            img: 'https://res.cloudinary.com/iro/image/upload/v1608043665/tweb/category/gym.png',
            description: 'Corporate Universe'
          },
          { 
            img: 'https://res.cloudinary.com/iro/image/upload/v1615454562/tweb/category/3094851.svg',
            description: 'Contract Domain'
          },
          { 
            img: 'https://res.cloudinary.com/iro/image/upload/v1615454562/tweb/category/3094851.svg',
            description: 'Investor Relations'
          },
          { 
            img: 'https://res.cloudinary.com/iro/image/upload/v1615454562/tweb/category/3094851.svg',
            description: 'Dispute Portfolio'
          },
          { 
            img: 'https://res.cloudinary.com/iro/image/upload/v1615454486/tweb/category/2910768.svg',
            description: 'Minute Book'
          },
          { 
            img: 'https://res.cloudinary.com/iro/image/upload/v1615454486/tweb/category/182321.svg',
            description: 'Reporting Total'
          },
          { 
            img: 'https://res.cloudinary.com/iro/image/upload/v1615454486/tweb/category/639394.svg',
            description: 'Attendance Register'
          },
        ]
      }
    }
  }
</script>

<style lang="scss">
  .onboarding-right {
    background: #ffffff;
    padding: 50px 180px 50px 90px;
    .start-card {
      outline: 0;
      border: 0;
      padding: 15px 20px;
      box-shadow: 0 1rem 3rem rgba(241,245,255,255) !important;
    }
    .basic-card {
      border: 1px solid #4982ff;
      background: #f6f9ff;
      border-radius: 10px;
      position: relative;
      padding: 20px 30px;
      .check {
        position: absolute;
        top: -15px;
        right: -15px;
      }
    }
    .module {
      border-bottom: 3px dashed #c5d7ff;
      .active {
        background: #fffae5;
        font-weight: bold;
        color: #000 !important;
      }
      .module-item {
        &:hover {
          background: #fffae5;
          font-weight: bold;
          color: #000 !important;
          }
      }
      .module-header {
        position: relative;
        margin-bottom: 10px;
        margin-left: 20px;
        &:before {
          content: '';
          height: 1px;
          width: 25px;
          position: absolute;
          left: -30px;
          top: 12px;
          background-color: #a7a6a6;
        }
        &:after {
          content: '';
          height: 1px;
          width: 87%;
          position: absolute;
          right: 0;
          top: 12px;
          background-color: #a7a6a6;
        }
      }
    }
  }
</style>