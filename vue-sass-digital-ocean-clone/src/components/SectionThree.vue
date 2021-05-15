<template>

<div class="container-solutions">

  <h2>{{titles.title}}</h2>
  <p>{{titles.subtitle}}</p>

  <div class="container">
    <div class="square" v-for="square in squares" :key="square.id">
      <img :src="square.icon" alt="">
      <h3>{{square.title}}</h3>
      <div>{{square.text}}</div>
      <a href="">{{square.link}}</a>
    </div>
  </div>

</div>

</template>

<script>
const titles =
{
  title:"Simple solutions for complex issues",
  subtitle: "Running a business is hard. Your cloud doesn’t have to be."
};

const squares = [
  {
    id:1,
    icon:"https://prismic-io.s3.amazonaws.com/www-static/1084f77c-6b8f-4617-aef9-7e29bf6bdc26_icon-web-mobile-apps.svg",
    title:"Web & mobile apps",
    text:"Create and run your web and mobile apps’ backends with lightning speed.",
    link:"Web & mobile app development."
  },
  {
    id:2,
    icon:"https://prismic-io.s3.amazonaws.com/www-static/0e5f957f-b54d-472f-bc13-30c90b8de213_icon-web-hosting.svg",
    title:"Website hosting",
    text:"Easily and reliably host a website for your business while keeping complete control of the underlying infrastructure.",
    link:"Website hosting in the cloud"
  },
  {
    id:3,
    icon:"https://prismic-io.s3.amazonaws.com/www-static/e4b85240-5a1a-45c0-9c5a-883bd5b49936_icon-web-mobile-apps.svg",
    title:"Streaming",
    text:"We provide the combination of flexible compute layers with low-bandwidth pricing that make building a streaming service easy for your developers – and cost-efficient for your business.",
    link:"Streaming compute services"
  },
  {
    id:4,
    icon:"https://prismic-io.s3.amazonaws.com/www-static/560096ba-e85f-4507-8bee-5422ce59eab2_icon-web-hosting.svg",
    title:"Gaming",
    text:"Build your game on DigitalOcean with flexible compute options and low-bandwidth pricing that will allow you to scale your game as fast as you want.",
    link:"Gaming development"
  },
  {
    id:5,
    icon:"https://prismic-io.s3.amazonaws.com/www-static/ef3bcfec-1d19-4735-a680-bc36fc689005_icon-big-data.svg",
    title:"Big data",
    text:"Run both batch and streaming big data workloads. Gain valuable insights that help inform business initiatives, improve your customer experience, and drive business growth.",
    link:"Big Data workloads"
  },
  {
    id:6,
    icon:"https://prismic-io.s3.amazonaws.com/www-static/32d546be-d238-441b-a3ee-4e63a8c28b71_icon-managed-services.svg",
    title:"Managed services",
    text:"Deploy and integrate any type of managed service – including SaaS, PaaS, DBaaS, and API – using our developer-friendly cloud platform. ",
    link:"Managed services in the cloud"
  },
  {
    id:7,
    icon:"https://images.prismic.io/www-static/f3553620-11f2-4b7c-b834-04709492d891_icon-web-hosting.png?auto=compress,format",
    title:"For agencies and web dev shops",
    text:"By providing a combination of flexible compute layers with low pricing, we empower you to create more powerful websites and applications for your clients at a lower cost than other cloud providers.",
    link:"Agency and Web Dev shop solutions"
  },
  {
    id:8,
    icon:"https://images.prismic.io/www-static/af2ef245-7192-4658-b9fc-26a649414cdc_icon-web-mobile-apps.png?auto=compress,format",
    title:"SaaS Solutions",
    text:"With flexible compute options combined with a host of other tools – including Managed Databases and Kubernetes – you can build your SaaS exactly how you want while saving on hosting costs.",
    link:"SaaS development platform"
  },
  {
    id:9,
    icon:"https://prismic-io.s3.amazonaws.com/www-static/560096ba-e85f-4507-8bee-5422ce59eab2_icon-web-hosting.svg",
    title:"Startups",
    text:"We ensure your cloud bills are predictable and affordable, while providing your business with a range of powerful compute options and networking tools that will scale with your business.",
    link:"Build your startup in the cloud"
  }
]
export default {
  name: 'SectionThree',
  props: {
    msg: String
  },
  data() {
    return {
      titles,squares
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../../public/style/positions.scss';
@import '../../public/style/color.scss';
@import '../../public/style/ui.scss';

.container-solutions{
  background-color: $color-white;
  h2,p{
    text-align: center;
    padding: 0 15px;
  }
  h2{
    font-size: 36px;
    color: $color-blue-write;
    margin: 100px 0 25px 0;
  }
  p{
    font-size: 20px;
    color: $color-grey-two;
    margin-bottom: 100px;
    font-weight: 300;
  }
  .container{
    width: 1170px;
    margin: 0 auto;
    @include row-sp-w;
    @media screen and (min-width: 360px) and (max-width: 1200px) {
    @include col-c-c;
    width: 70vw
    }
    .square{
      width: 330px;
      margin-bottom: 50px;
      @media screen and (min-width: 360px) and (max-width: 1200px) {
      @include col-c-c;
      width: 70vw;
     }
      h3{
        color: $color-blue-write;
        font-size: 18px;
        margin: 20px 0;
      }
      div{
        color: $color-grey-two;
        margin-bottom: 20px;
        width: 100%;
        @media screen and (min-width: 360px) and (max-width: 1200px) {
        text-align: center;
     }
      }
      a{
        text-decoration: none;
        color: $color-blue;
      }
    }
  }
}
</style>