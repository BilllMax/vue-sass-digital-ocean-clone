<template>

<div class="container-business">
  <h2>{{titles.title}}</h2>
  <p>{{titles.subtitle}}</p>

  <div class="square-container">
  <div class="square" v-for="item in square" :key="item.id">
    <img :src="item.icon" alt="">
    <h3>{{item.title}}</h3>
    <div class="text">{{item.text}}</div>
    <!-- <div class="ver" v-for="pino in over" :key="pino">{{pino}}</div> -->
  </div>
  <div class="square last-square">
    <p>View our product portfolio</p>
    <!-- <div class="ver"></div> -->
  </div>
  </div>
</div>

</template>

<script>
const titles =
{
  title:"Tailored for growing businesses",
  subtitle:"Develop, manage, and scale your applications on DigitalOcean’s complete cloud platform."
};

const square = [
  {
    id:1,
    icon:"https://prismic-io.s3.amazonaws.com/www-static/9a0e17ef-cd6e-432d-a137-28713dbb6b5d_icon-compute.svg",
    title:"Compute",
    text:"Confidently build and release with scalable compute products in the cloud."
  },
  {
    id:2,
    icon:"https://prismic-io.s3.amazonaws.com/www-static/f0f46213-f267-4c25-b813-5f7350908b23_icon-databases.svg",
    title:"Database",
    text:"Optimize your application’s performance with fully managed databases."
  },
  {
    id:3,
    icon:"https://prismic-io.s3.amazonaws.com/www-static/f54297ed-68b7-4e7a-ae81-8d2e81d4a102_icon-storage.svg",
    title:"Storage",
    text:"With highly available and scalable storage options, you can store and quickly access any amount of data."
  },
  {
    id:4,
    icon:"https://prismic-io.s3.amazonaws.com/www-static/75057db5-c881-4d05-b24e-052bed4e7a25_icon-networking.svg",
    title:"Networking",
    text:"Secure resources and route applications with highly reliable and customizable networking products."
  },
  {
    id:5,
    icon:"https://prismic-io.s3.amazonaws.com/www-static/3926c760-a868-4c24-a1c9-8a8b9f097544_icon-marketplace.svg",
    title:"Marketplace",
    text:"Build faster and smarter with a diverse catalog of preconfigured."
  }
];

// const over = [
//   {
//     id:1,
//     voice:["Droplets","Kubernetes","App Platform"]
//   },
//   {
//     id:2,
//     voice:["MySQL","PostgreSQL","Redis"]
//   },
//   {
//     id:3,
//     voice:["Block Storage","Object Storage"]
//   },
//   {
//     id:4,
//     voice:["Firewalls","Load Balancers","DNS","Private Networking"]
//   },
//   {
//     id:5,
//     voice:["Marketplace"]
//   }
// ]
// const over = ["a","b"]
export default {
  name: 'SectionOne',
  props: {
    msg: String
  },
  data() {
    return {
      titles,square
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../../public/style/positions.scss';
@import '../../public/style/color.scss';
@import '../../public/style/ui.scss';

.container-business{
  min-height: 940px;
  background: url("https://prismic-io.s3.amazonaws.com/www-static/e2b726ab-087a-4e53-8aca-65826c3f93e7_bg-grid.svg");
  @include col-fs-c;
  h2{
    color:$color-blue-write;
    font-size: 36px;
    font-weight: 900;
    margin-top: 50px;
    @media screen and (min-width: 360px) and (max-width: 1000px) {
    max-width: 80%;
    }
  }
  p{
    color:$color-grey-two;
    font-size: 20px;
    margin: 25px 0;
    @media screen and (min-width: 360px) and (max-width: 1000px) {
    max-width: 80%;
    text-align: center;
    }
  }
  .square-container{
    width: 945px;
    margin: 0 auto;
    @include row-sp-w;
    @media screen and (min-width: 360px) and (max-width: 1000px) {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      width: 100vw;
    }
    .square{
      width: 275px;
      height: 295px;
      margin-bottom: 30px;
      padding: 15px 0 0 15px;
      background-color: $color-white;
      box-shadow: 5px 5px 15px -9px rgba(0,0,0,0.35);
      @media screen and (min-width: 360px) and (max-width: 1000px) {
        width: 90%;
        padding: 0px;
        @include col-c-c;
      }
      // .ver{
      //   position: absolute;
      //   top: 0;
      //   left: 0;
      //   background-color: chartreuse;
      //   width: 100%;
      //   height: 100%;
      //   opacity: 0;
      // }
      h3{
        margin: 15px 0;
        color: $color-blue-write;
        font-size: 25px;
      }
      .text{
        font-size: 16px;
        line-height: 26px;
        color: $color-blue-write;
        @media screen and (min-width: 360px) and (max-width: 1000px) {
          max-width: 80%;
        }
      }
    }
    .square:hover .ver{
      opacity: 1;
    }
    .last-square{
      @include col-c-c;
      position: relative;
      cursor: pointer;
      p{
        color: $color-blue;
        text-align: center;
        width: 70%;
        font-size: 16px;
      }
    }
  }
}
</style>
