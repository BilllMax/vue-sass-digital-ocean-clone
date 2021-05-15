<template>

<div class="container-hot">
  <h2>{{titles.title}}</h2>
  <p>{{titles.subtitle}}</p>

  <div class="container">

    <div class="square" v-for="item in square" :key="item.id">
      <img :src="item.icon" alt="">
      <div class="txt">
        <h3>{{item.title}}</h3>
        <div>{{item.text}}</div>
        <a href="">{{item.link}}</a>
      </div>
    </div>

  </div>

</div>

</template>

<script>
const titles = {
  title:"Host mission-critical solutions",
  subtitle:"Everything you need to run fast and scale faster."
}

const square = [
  {
    id:1,
    icon:"https://images.prismic.io/www-static/a61f0779-e2d3-4bc0-a5b7-f86a570d97b6_biz-control-your-costs.jpg?auto=compress,format",
    title:"Control your costs",
    text:"We offer transparent, predictable pricing so you know what you’ll be paying every single time. Cloud Spectator – an independent benchmarking firm – concluded that DigitalOcean delivers the best CPU performance per dollar when compared with AWS and Google.",
    link:"View the report"
  },
  {
    id:2,
    icon:"https://images.prismic.io/www-static/ea7aa838-a352-4240-b9f4-c60576843fc6_biz-protect-your-information.jpg?auto=compress,format",
    title:"Protect your information",
    text:"Our data centers are individually audited and certified by various internationally recognized compliance standards, including SOC 1, SOC 2, PCI-DSS, ISO/IEC 27001:2013 Certification and EU-U.S. and Swiss-U.S. Privacy Shield Certification.",
    link:"Learn more"
  },
  {
    id:3,
    icon:"https://images.prismic.io/www-static/c29722f7-089e-410e-874b-d5b5e8c28a8e_biz-automate.jpg?auto=compress,format",
    title:"Automate & orchestrate with a click",
    text:"Configure, manage, and scale your infrastructure using popular one-click DevOps tools. Leverage our API and open source libraries to easily manage resources.",
    link:""
  },
    {
    id:4,
    icon:"https://images.prismic.io/www-static/12213ebe-2a84-4084-9178-c02a4675bbee_biz-global-availability.jpg?auto=compress,format",
    title:"Get global availability",
    text:"Deliver a great user experiences with 99.99% uptime across eight data centers in 12 worldwide regions.",
    link:"Learn more"
  },
  {
    id:5,
    icon:"https://images.prismic.io/www-static/47de596e-da7f-4da3-b4f2-24ce5b2784ac_biz-team-accounts.jpg?auto=compress,format",
    title:"Collaborate with team accounts",
    text:"Enable unified collaboration with distinct user roles, one invoice, and no shared credentials.",
    link:""
  },
  {
    id:6,
    icon:"https://images.prismic.io/www-static/7f7b6732-3cb6-4c2d-a15c-4a0a18725b9f_biz-support.jpg?auto=compress,format",
    title:"Protect your information",
    text:"When you need help, get free around-the-clock technical support – or go in depth with Premier Support if your business needs a high-touch, personalized support experience.",
    link:"Learn more"
  }
]
export default {
  name: 'SectionFour',
  props: {
    msg: String
  },
  data() {
    return {
      titles,square
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../../public/style/positions.scss';
@import '../../public/style/color.scss';
@import '../../public/style/ui.scss';

.container-hot{
  background-color: $color-white;
  h2,p{
    text-align: center;
  }
  h2{
  font-size: 36px;
  color: $color-blue-write;
  margin: 100px 0 25px 0;
  }
  p{
    font-size: 20px;
    font-weight: 300;
    color: $color-grey-two;
    margin-bottom: 100px;
  }
}

.container{
  width: 1170px;
  margin: 0 auto;
  @include row-sp-w;
  @media screen and (min-width: 360px) and (max-width: 1200px) {
  @include col-c-c;
  width: 100vw;
  }

  .square{
    width: 550px;
    display: flex;
    padding-bottom: 50px;
    margin-bottom: 25px;
    @media screen and (min-width: 601px) and (max-width: 1200px) {
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    width: 50vw;
    }
    @media screen and (min-width: 360px) and (max-width: 600px) {
    width: 70vw;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    }

    .txt{
      width: 100%;
      h3{
        color:$color-blue-write;
        margin-bottom: 25px;
        font-size: 18px;
      }
      div{
        margin-bottom: 25px;
        color: $color-grey-two;
        line-height: 25px;
        font-size: 16px;
        @media screen and (min-width: 360px) and (max-width: 1200px) {
          width: 100%;
          text-align: center;
        }
      }
      a{
        text-decoration: none;
        color: $color-blue;
      }
    }
    img{
      min-width: 160px;
      height: 128px;
    }
  }
}
</style>