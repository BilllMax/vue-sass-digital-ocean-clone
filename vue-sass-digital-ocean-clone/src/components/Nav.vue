<template>
<nav>

  <div class="up">

    <div class="left">

      <div class="nav-btn">
        {{upLeft.btn}}
      </div>
      <div class="slogan">
        {{upLeft.slogan}} 
      </div>

    </div>

    <div class="right">
      <ul class="uplist">
        <li v-for="item in upRight" :key="item">{{item}}</li>
      </ul>
    </div>

  </div>

  <hr>

  <div class="down">
    <div class="down-left">
      <img :src="logonav.logo" alt="">
      <ul class="downlist">
        <!-- <li v-for="item in down" :key="item">{{item}}</li> -->
        <li v-on:click="toggleMode()">Products <i class="fas fa-chevron-down"></i></li>
        <li v-on:click="toggleModeTwo()">Solutions <i class="fas fa-chevron-down"></i></li>
        <li>Marketplace</li>
        <li>Customers</li>
        <li v-on:click="toggleModeThree()">Community <i class="fas fa-chevron-down"></i></li>
        <li>Pricing</li>
      </ul>
    </div>
    <div class="down-right">
      <div class="btn-nav white">Sign in</div>
      <div class="btn-nav blue">Sign up</div>
    </div>
  </div>
</nav>

<div v-show="!active" class="dropdown-products">
  <div class="up">
    <div class="left">
      <div  v-for="item in dropDownOne" :key="item" class="rectangle">
        <h5>{{item.title}}</h5>
        <div>{{item.subtitle}}</div>
        <div class="icon">
          <i class="fas fa-chevron-right"></i>
        </div>
      </div>
    </div>
    <div class="right">
      <div class="block">
        <ul>
          <li>{{dropDownOneRight[0].title}}</li>
          <li>{{dropDownOneRight[0].item}}</li>
          <li>{{dropDownOneRight[0].item2}}</li>
          <li>{{dropDownOneRight[0].item3}}</li>
        </ul>
        <ul>
          <li>{{dropDownOneRight[3].title}}</li>
          <li>{{dropDownOneRight[3].item}}</li>
          <li>{{dropDownOneRight[3].item2}}</li>
        </ul>
      </div>
      <div class="block">
        <ul>
          <li>{{dropDownOneRight[1].title}}</li>
          <li>{{dropDownOneRight[1].item}}</li>
          <li>{{dropDownOneRight[1].item2}}</li>
          <li>{{dropDownOneRight[1].item3}}</li>
        </ul>
        <ul>
          <li>{{dropDownOneRight[4].title}}</li>
          <li>{{dropDownOneRight[4].item}}</li>
          <li>{{dropDownOneRight[4].item2}}</li>
          <li>{{dropDownOneRight[4].item3}}</li>
          <li>{{dropDownOneRight[4].item4}}</li>
          <li>{{dropDownOneRight[4].item5}}</li>
        </ul>
      </div>
      <div class="block">
        <ul>
          <li>{{dropDownOneRight[2].title}}</li>
          <li>{{dropDownOneRight[2].item}}</li>
          <li>{{dropDownOneRight[2].item2}}</li>
          <li>{{dropDownOneRight[2].item3}}</li>
          <li>{{dropDownOneRight[2].item4}}</li>
          <li>{{dropDownOneRight[2].item5}}</li>
          <li>{{dropDownOneRight[2].item6}}</li>
        </ul>
      </div>
    </div>
  </div>
  <div class="down">
    <div>See all products</div>
    <i class="fas fa-chevron-right"></i>
  </div>
</div>

<div v-show="!active2" class="dropdown-solutions">
  <div class="top">OUR SOLUTIONS</div>
  <div class="middle">
    <div v-for="item in dropDownTwo" :key="item" class="block-two">
      <div>{{item.title}}</div>
      <div>{{item.subtitle}}</div>
      <div class="icon">
        <i class="fas fa-chevron-right"></i>
      </div>
    </div>
  </div>
  <div class="bottom">
    <div>See all products</div>
    <i class="fas fa-chevron-right"></i>
  </div>
</div>

<div v-show="!active3"  class="dropdown-community">
    <div class="left">
      <div  v-for="item in dropDownComLeft" :key="item" class="rectangle">
        <h5>{{item.title}}</h5>
        <div>{{item.subtitle}}</div>
        <div class="icon">
          <i class="fas fa-chevron-right"></i>
        </div>
      </div>
    </div>
    <div class="right">
      <div class="r-left">
        <ul>
          <li v-for="item in dropDownComRRight " :key="item">{{item}}</li>
        </ul>
      </div>
      <div class="r-right">
        <div class="up">FEATURED ARTICLES</div>
        <div v-for="item in dropDownComRLeft" :key="item" class="block-three">
          <img :src="item.img" alt="">
          <div>{{item.item1}}</div>
        </div>
      </div>
    </div>
</div>

<div class="resp-nav">
  <img :src="logonav.logo" alt="">
  <i v-on:click="active4 = !active4" class="fas fa-bars"></i>
</div>

<div v-show="!active4" class="hamburger">

  <div class="products">
  <div class="up">
    <div class="left">
      <div class="product-title">Products</div>
      <div  v-for="item in dropDownOne" :key="item" class="rectangle">
        <h5>{{item.title}}</h5>
        <div>{{item.subtitle}}</div>
        <div class="icon">
          <i class="fas fa-chevron-right"></i>
        </div>
      </div>
    </div>
    <div class="right">
      <div class="block">
        <ul>
          <li>{{dropDownOneRight[0].title}}</li>
          <li>{{dropDownOneRight[0].item}}</li>
          <li>{{dropDownOneRight[0].item2}}</li>
          <li>{{dropDownOneRight[0].item3}}</li>
        </ul>
        <ul>
          <li>{{dropDownOneRight[3].title}}</li>
          <li>{{dropDownOneRight[3].item}}</li>
          <li>{{dropDownOneRight[3].item2}}</li>
        </ul>
      </div>
      <div class="block">
        <ul>
          <li>{{dropDownOneRight[1].title}}</li>
          <li>{{dropDownOneRight[1].item}}</li>
          <li>{{dropDownOneRight[1].item2}}</li>
          <li>{{dropDownOneRight[1].item3}}</li>
        </ul>
        <ul>
          <li>{{dropDownOneRight[4].title}}</li>
          <li>{{dropDownOneRight[4].item}}</li>
          <li>{{dropDownOneRight[4].item2}}</li>
          <li>{{dropDownOneRight[4].item3}}</li>
          <li>{{dropDownOneRight[4].item4}}</li>
          <li>{{dropDownOneRight[4].item5}}</li>
        </ul>
      </div>
      <div class="block">
        <ul>
          <li>{{dropDownOneRight[2].title}}</li>
          <li>{{dropDownOneRight[2].item}}</li>
          <li>{{dropDownOneRight[2].item2}}</li>
          <li>{{dropDownOneRight[2].item3}}</li>
          <li>{{dropDownOneRight[2].item4}}</li>
          <li>{{dropDownOneRight[2].item5}}</li>
          <li>{{dropDownOneRight[2].item6}}</li>
        </ul>
      </div>
    </div>
  </div>
  <div class="down">
    <div>See all products</div>
    <i class="fas fa-chevron-right"></i>
  </div>
  </div>

  <div class="solutions">
    <div class="product-solution">Products</div>
  <div class="top">OUR SOLUTIONS</div>
  <div class="middle">
    <div v-for="item in dropDownTwo" :key="item" class="block-two">
      <div>{{item.title}}</div>
      <div>{{item.subtitle}}</div>
      <div class="icon">
        <i class="fas fa-chevron-right"></i>
      </div>
    </div>
  </div>
  <div class="bottom">
    <div>See all products</div>
    <i class="fas fa-chevron-right"></i>
  </div>
  </div>

  <div class="community">
    <div class="left">
      <div  v-for="item in dropDownComLeft" :key="item" class="rectangle">
        <h5>{{item.title}}</h5>
        <div>{{item.subtitle}}</div>
        <div class="icon">
          <i class="fas fa-chevron-right"></i>
        </div>
      </div>
    </div>
    <div class="right">
      <div class="r-left">
        <ul>
          <li v-for="item in dropDownComRRight " :key="item">{{item}}</li>
        </ul>
      </div>
      <div class="r-right">
        <div class="up">FEATURED ARTICLES</div>
        <div v-for="item in dropDownComRLeft" :key="item" class="block-three">
          <img :src="item.img" alt="">
          <div>{{item.item1}}</div>
        </div>
      </div>
    </div>
</div>

</div>

</template>

<script>
const upLeft = {
  btn:"LEARN MORE",
  slogan:"Check out the latest DigitalOcean Currents Survey Report on Open Source"
};

const upRight = ["Blog","Docs","Get Support", "Sales"];

const logonav = {
  logo:"https://images.prismic.io/www-static/49aa0a09-06d2-4bba-ad20-4bcbe56ac507_logo.png?auto=compress,format"
};

const down = ["Products ","Solutions ", "Marketplace", "Customers", "Community ", "Pricing"];

const dropDownOne = [
{
title:"FEATURED PRODUCTS",
subtitle:""
},
{
title:"Droplets",
subtitle:"Scalable virtual machines"
},
{
title:"Kubernetes",
subtitle:"Managed Kubernetes clusters"
},
{
title:"App Platform",
subtitle:"Get apps to market faster"
},
{
title:"Databases",
subtitle:"Worry-free setup & maintenance"
},
{
title:"Spaces",
subtitle:"Simple object storage"
}
];

const dropDownOneRight = [
{
title:"COMPUTE",
item:"Droplets",
item2:"Kubernetes",
item3:"App Platform"
},
{
title:"MANAGED DATABASES",
item:"MySQL",
item2:"PostgreSQL",
item3:"Redis™"
},
{
title:"DEVELOPER TOOLS",
item:"API",
item2:"CLI",
item3:"Monitoring",
item4:"Teams",
item5:"Deploy to DigitalOcean button",
item6:"Support"
},
{
title:"STORAGE",
item:"Spaces Object Storage",
item2:"Volumes Block Storage"
},
{
title:"NETWORKING",
item:"Virtual Private Cloud (VPC)",
item2:"Cloud Firewalls",
item3:"Load Balancers",
item4:"Floating IPs",
item5:"DNS"
}
];

const dropDownTwo = [
  {
    title:"Website Hosting",
    subtitle:"Easily and reliably host a website"
  },
  {
    title:"Web & Mobile Apps",
    subtitle:"Quickly build and reliably run your apps"
  },
  {
    title:"Video Streaming Hosting",
    subtitle:"Create a highly available streaming service"
  },
  {
    title:"Gaming Development",
    subtitle:"Scale your game as fast as you want"
  },
  {
    title:"Cloud VPN",
    subtitle:"Quickly set up a fast, reliable, and easy to use VPN"
  },
  {
    title:"Big Data Computing",
    subtitle:"Run batch and streaming big data workloads"
  },
  {
    title:"Startups",
    subtitle:"A cloud partnership to power your startup"
  },
  {
    title:"SaaS Development",
    subtitle:"Build your SaaS exactly how you want"
  },
  {
    title:"Agency & Web Dev Shops",
    subtitle:"Create powerful websites and applications for your clients"
  },
  {
    title:"Managed Cloud Hosting Providers",
    subtitle:"We make cloud hosting simple and cost-efficient"
  }
];

const dropDownComLeft = [
{
title:"COMMUNITY",
subtitle:""
},
{
title:" Overview",
subtitle:"Connect, share and learn"     
},
{
title:"Kubernetes",
subtitle:"Managed Kubernetes clusters"
},
{
title:"Tutorials",
subtitle:"DevOps and development guides"                                                                                                    
},
{
title:"Questions and Answers",
subtitle:"Development and systems Q&A"
},
{
title:"Tools",
subtitle:"Community-built integrations"
}
];

const dropDownComRRight = [
"GET INVOLVED",
"Write for DOnations",
"Meetups",
"Hatch Startup Program",
"Open Source Sponsorships",
"Hacktoberfest"
];

const dropDownComRLeft =[
  {
    img:"https://images.prismic.io/www-static/63808eba4b5c17be2c07d709771310e1ce75b6b6_article-1.jpg?auto=compress,format",
    item1:"How to Deploy a PHP Application with Kubernetes on Ubuntu 16.04"
  },
    {
    img:"https://images.prismic.io/www-static/cf6d27910f0fd823c5d494cf3ca833a786c106c5_article-2.jpg?auto=compress,format",
    item1:"Understanding Database Sharding"
  },
  {
    img:"https://images.prismic.io/www-static/3644243d4edcb457a5ad46f2eb3b858e846c8659_article-3.jpg?auto=compress,format",
    item1:"How to Build a Node.js Application with Docker"
  }
];

export default {
  name: 'Nav',
  props: {
    msg: String
  },
  data() {
    return {
      upLeft,
      upRight,
      logonav,
      down,
      dropDownOne,
      dropDownOneRight,
      dropDownTwo,
      dropDownComLeft,
      dropDownComRRight,
      dropDownComRLeft,
      active:true,
      active2:true,
      active3:true,
      active4:true,
    }
  },
  methods:{
    toggleMode() {
      this.active2 = true;
      this.active3 = true;
      this.active = !this.active;
    },
    toggleModeTwo() {
      this.active3 = true;
      this.active = true;
      this.active2 = !this.active2;
    },
    toggleModeThree() {
      this.active = true;
      this.active2 = true;
      this.active3 = !this.active3;
    },
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../../public/style/positions.scss';
@import '../../public/style/color.scss';
@import '../../public/style/ui.scss';
nav{
  position: fixed;
  top: 0;
  width: 100%;
  background-color: $color-white;
  height: 111px;
  @media screen and (min-width: 360px) and (max-width: 1200px) {
    display: none;
  }
  .up{
    height: 38px;
    width: 99%;
    margin: 0 auto;
    @include row-sb-c;
    
    .left{
      width: 500px;
      @include row-c;
      .nav-btn{
        width: 75px;
        height: 20px;
        margin-right: 20px;
        @include col-c-c;
        font-size: 10px;
        border-radius: 5px;
        background-color: $color-btn-nav;
        cursor: pointer;
      }
      .slogan{
        font-size: 11px;
        color: $color-grey-two;
      }
    }
    .right{
      width: 20% ;
      @include row-end;
      .uplist{
        display: flex;
        li{
          font-size: 12px;
          color: $color-grey-two;
          cursor: pointer;
        }
        li:first-child,li:nth-child(2),li:nth-child(3){
          margin-right: 10px;
        }
      }
    }
  }
  hr{
    border: 1px solid $color-grey;
  }
  .down{
    width: 99%;
    margin: 0 auto;
    height: 71px;
    @include row-sb;
    .down-left{
      width: 800px;
      @include row-st-c;
      img{
        width: 172px;
        height: 28px;
      }
      .downlist{
        @include row-st-c;
        li{
          margin-right: 15px;
          font-size: 14px;
          font-weight: 600;
          color: $color-blue-write;
          cursor: pointer;
          @include row-st-c;
          i{
            margin-left: 5px;
            color: $color-grey-two;
            opacity: 0.5;
          }
        }
      }
    }
    .down-right{
      width: 200px;
      @include row-sb-c;
      .btn-nav{
        height: 40px;
        width: 80px;
        @include col-c-c;
        border-radius: 5px;
        font-weight: bolder;
        cursor: pointer;
      }
      .white{
        color: $color-blue;
        border: 1px solid $color-blue;
      }
      .blue{
        background-color: $color-blue;
        color:$color-white;
      }
    }
  }
}

.dropdown-products{
  position: absolute;
  left: 5%;
  width: 1200px;
  height:570px ;
  z-index: 2;
  top: 111px;
  background-color: $color-white;
  .up{
    height: 90%;
    width: 100%;
    display: flex;
    .left{
      width: 35%;
      height: 100%;
      background-color: $color-background-dropdown;
      @include col-c-c;
      .rectangle:first-child{
          h5{
            color: $color-blue;
            font-size: 12px;
          }
          pointer-events: none;
      }
      .rectangle{
        width: 70%;
        height: 65px;
        margin-bottom: 5px;
        border-radius: 5px;
        display: flex;
        flex-direction: column;
        padding:0px 15px;
        position: relative;
        cursor: pointer;
        &:hover{
          background-color: $dropdown-hover;
        }
        &:hover .icon{
          opacity: 1;
        }
        &:hover h5{
        color:$color-blue;
        }
        h5{
          margin: 10px 0 5px 0;
          color: $color-blue-write;
          font-size: 15px;
        }
        div{
          color: $color-grey-two;
          font-size: 14px;
        }
        .icon{
          width: 20px;
          height: 20px;
          border-radius: 50%;
          background-color: $color-blue;
          color: $color-white;
          font-size: 8px;
          position: absolute;
          top: 18px;
          right: 15px;
          @include col-c-c;
          opacity: 0;
        }
      }
    }
    .right{
      width: 65%;
      height: 100%;
      display: flex;
      .block{
        width: calc(33.33% - 40px);
        height: calc(100% - 50px);
        padding-top: 50px;
        padding-left: 40px;
        ul{
          list-style: none;
          padding: 0;
          color: $color-grey-two;
          font-size: 14px;
          margin-bottom: 90px;
          li:first-child{
            color: $color-blue-write;
            font-size: 15px;
            font-weight: bold;
            margin-bottom: 10px;
            pointer-events: none;
          }
          li{
            margin-bottom: 10px;
            cursor: pointer;
            &:hover{
              color: $color-blue;
            }
          }
        }
      }
      }
  }
  .down{
    height: calc(10% - 1px);
    width: 100%;
    border-top: 1px solid $color-grey;
    display: flex;
    justify-content: center;
    align-items: center;
    div{
      font-size: 12px;
      margin-right: 5px;
      cursor: pointer;
      &:hover{
        color: $color-blue;
      }
    }
    i{
      font-size: 10px;
      &:hover{
        color: $color-blue;
      }
    }
  }
}

.dropdown-solutions{
  width: 910px;
  height: 500px;
  position: absolute;
  border-radius: 5px;
  top: 111px;
  left:220px;
  background-color: $color-white;
  .top{
    width: calc(100% - 15px);
    padding-left: 15px;
    height: 20%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    color: $color-blue;
    font-weight: bold;
  }
  .middle{
    width: 100%;
    height: 70%;
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    align-items: center;
    .block-two{
      width: calc(49% - 30px);
      height: calc(20% - 5px);
      margin: 2.5px 0;
      padding: 0 15px;
      border-radius: 5px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      position: relative;
      cursor: pointer;
      &:hover{
        background-color: $dropdown-hover;
      }
      &:hover .icon{
        opacity: 1;
      }
      &:hover div:first-child{
        color: $color-blue;
      }
      div:first-child{
        color: $color-blue-write;
        font-size: 15px;
        font-weight: bold;
      }
      div:nth-child(2){
        color: $color-grey-two;
        font-size: 14px;
      }
      .icon{
        width: 20px;
        height: 20px;
        border-radius: 50%;
        background-color: $color-blue;
        color: $color-white;
        font-size: 8px;
        position: absolute;
        top: 20px;
        right: 15px;
        @include col-c-c;
        opacity: 0;
        }
    }
  }
  .bottom{
    height: calc(10% - 1px);
    width: 100%;
    border-top: 1px solid $color-grey;
    display: flex;
    justify-content: center;
    align-items: center;
    div{
      font-size: 12px;
      margin-right: 5px;
      cursor: pointer;
      &:hover{
        color: $color-blue;
      }
    }
    i{
      font-size: 10px;
      &:hover{
        color: $color-blue;
      }
    }
  }
}

.dropdown-community{
  display: flex;
  border-radius: 5px;
  position: absolute;
  right: 5%;
  width: 1200px;
  height:470px ;
  z-index: 2;
  top: 111px;
  background-color: $color-white;
      .left{
      width: 35%;
      height: 100%;
      background-color: $color-background-dropdown;
      @include col-c-c;
      .rectangle:first-child{
        height: 30px;
        margin: 0;
        overflow-y: hidden;
        margin-bottom: 25px;
          h5{
            color: $color-blue;
            font-size: 12px;
          }
          pointer-events: none;
      }
      .rectangle{
        width: 70%;
        height: 65px;
        margin-bottom: 5px;
        border-radius: 5px;
        display: flex;
        flex-direction: column;
        padding:0px 15px;
        position: relative;
        cursor: pointer;
        &:hover{
          background-color: $dropdown-hover;
        }
        &:hover h5{
          color:$color-blue;
        }
        &:hover .icon{
          opacity: 1;
        }
        h5{
          margin: 10px 0 5px 0;
          color: $color-blue-write;
          font-size: 15px;
          &:hover{
          color:$color-blue;
          }
        }
        div{
          color: $color-grey-two;
          font-size: 14px;
        }
        .icon{
          width: 20px;
          height: 20px;
          border-radius: 50%;
          background-color: $color-blue;
          color: $color-white;
          font-size: 8px;
          position: absolute;
          top: 18px;
          right: 15px;
          @include col-c-c;
          opacity: 0;
        }
      }
    }
    .right{
      width: 65%;
      height: 100%;
      display: flex;
      .r-left{
        width: 40%;
        height: calc(100% - 42.5px);
        padding-top: 42.5px;
        ul{
          li:first-child{
            font-size: 12px;
            color: $color-blue-write;
            font-weight: bold;
            margin-bottom: 35px;
            pointer-events: none;
          }
          li{
            margin-bottom: 15px;
            font-size: 14px;
            color: $color-grey-two;
            cursor: pointer;
            &:hover{
              color:$color-blue;
            }
          }
        }
      }
      .r-right{
        width: 60%;
        height: calc(100% - 42.5px);
        padding-top: 42.5px;
        .up{
          width: 100%;
          height: 10%;
          font-size: 12px;
          color: $color-blue-write;
          font-weight: bold;
        }
        .block-three{
          width: 100%;
          height: 15%;
          display: flex;
          align-items: center;
          img{
            width: 50px;
            height: 50px;
            border-radius: 15px;
            margin-right: 20px;
          }
          div{
            width: 80%;
            font-size: 14px;
            color: $color-grey-two;
            cursor: pointer;
            &:hover{
              color:$color-blue;
            }
          }
        }
      }
    }
}

.resp-nav{
  height: 75px;
  padding: 0 25px;
  display: none;
  @media screen and (min-width: 360px) and (max-width: 1200px) {
      @include row-sb-c;
  }
  img{
    width: 172px;
    height: 28px;
    cursor: pointer;
  }
  i{
    color: $color-grey-two;
    font-size: 20px;
    cursor: pointer;
  }
}

.hamburger{
  width: 95%;
  position: absolute;
  top: 80px;
  left:2.5%;
  z-index: 10;
  .products{
  width: 100%;
  background-color: $color-white;
  display: flex;
  flex-direction: column;
  .up{
    height: 90%;
    width: 100%;
    display: flex;
    flex-direction: column;
    .left{
      height: 500px;
      .rectangle:nth-child(2){
        overflow-y: hidden;
          h5{
            color: $color-blue;
            font-size: 15px;
          }
        pointer-events: none;         
      }
      .product-title{
        width: 95%;
        height: 50px;
        border-bottom: 2px solid $color-grey;
        margin:0 auto;
      }
      .rectangle{
        width: 300px;
        height: 65px;
        margin-left: 5px;
        margin-bottom: 5px;
        border-radius: 5px;
        display: flex;
        flex-direction: column;
        padding:0px 15px;
        position: relative;
        cursor: pointer;
        &:hover{
          background-color: $dropdown-hover;
        }
        &:hover .icon{
          opacity: 1;
        }
        &:hover h5{
        color:$color-blue;
        }
        h5{
          margin: 10px 0 5px 0;
          color: $color-blue-write;
          font-size: 15px;
        }
        div{
          color: $color-grey-two;
          font-size: 14px;
        }
        .icon{
          width: 20px;
          height: 20px;
          border-radius: 50%;
          background-color: $color-blue;
          color: $color-white;
          font-size: 8px;
          position: absolute;
          top: 18px;
          right: 15px;
          @include col-c-c;
          opacity: 0;
        }
      }
    }
    .right{
      width: 65%;
      display: flex;
      flex-direction: column;
      .block{
        ul{
          list-style: none;
          padding: 0;
          color: $color-grey-two;
          font-size: 14px;
          padding-left: 18px;
          li:first-child{
            color: $color-blue-write;
            font-size: 15px;
            font-weight: bold;
            margin-bottom: 10px;
            pointer-events: none;
          }
          li{
            margin-bottom: 10px;
            cursor: pointer;
            &:hover{
              color: $color-blue;
            }
          }
        }
      }
      }
  }
  .down{
    height: 30px;
    width: 100%;
    border-top: 1px solid $color-grey;
    display: flex;
    justify-content: center;
    align-items: center;
    div{
      font-size: 12px;
      margin-right: 5px;
      cursor: pointer;
      &:hover{
        color: $color-blue;
      }
    }
    i{
      font-size: 10px;
      cursor: pointer;
      &:hover{
        color: $color-blue;
      }
    }
  }
  }
  .solutions{
  width: 100%;
  background-color: $color-white;
    .product-solution{
    width: 95%;
    height: 50px;
    border-bottom: 2px solid $color-grey;
    margin:15px;
    }
  .top{
    width: calc(100% - 15px);
    padding-left: 15px;
    height: 20%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    color: $color-blue;
    font-weight: bold;
    margin-top: 50px;
  }
  .middle{
    width: 100%;
    height: 70%;
    display: flex;
    flex-direction: column;
    .block-two{
      width: calc(85vw - 12.5px);
      height: 65px;
      margin: 2.5px 5px;
      padding: 0 12.5px;
      border-radius: 5px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      position: relative;
      cursor: pointer;
      &:hover{
        background-color: $dropdown-hover;
      }
      &:hover .icon{
        opacity: 1;
      }
      &:hover div:first-child{
        color: $color-blue;
      }
      div:first-child{
        color: $color-blue-write;
        font-size: 15px;
        font-weight: bold;
      }
      div:nth-child(2){
        color: $color-grey-two;
        font-size: 14px;
      }
      .icon{
        width: 20px;
        height: 20px;
        border-radius: 50%;
        background-color: $color-blue;
        color: $color-white;
        font-size: 8px;
        position: absolute;
        top: 20px;
        right: 15px;
        @include col-c-c;
        opacity: 0;
        }
    }
  }
  .bottom{
    height: 30px;
    width: 100%;
    border-top: 1px solid $color-grey;
    display: flex;
    justify-content: center;
    align-items: center;
    div{
      font-size: 12px;
      margin-right: 5px;
      cursor: pointer;
      &:hover{
        color: $color-blue;
      }
    }
    i{
      font-size: 10px;
      cursor: pointer;
      &:hover{
        color: $color-blue;
      }
    }
  }
  }
  .community{
  display: flex;
  flex-direction: column;
  width: 100%;
  background-color: $color-white;
  padding-bottom: 25px;
      .left{
      height: 100%;
      .rectangle:first-child{
        height: 40px;
        margin: 0;
        overflow-y: hidden;
        margin-bottom: 25px;
          h5{
            color: $color-blue;
            font-size: 15px;
            margin-left: 5px;
          }
          pointer-events: none;
      }
      .rectangle{
        height: 65px;
        width: 300px;
        margin-left: 5px;
        padding-left: 12.5px;
        margin-bottom: 5px;
        border-radius: 5px;
        display: flex;
        flex-direction: column;
        position: relative;
        cursor: pointer;
        &:hover{
          background-color: $dropdown-hover;
        }
        &:hover h5{
          color:$color-blue;
        }
        &:hover .icon{
          opacity: 1;
        }
        h5{
          margin: 10px 0 5px 0;
          color: $color-blue-write;
          font-size: 15px;
          &:hover{
          color:$color-blue;
          }
        }
        div{
          color: $color-grey-two;
          font-size: 14px;
        }
        .icon{
          width: 20px;
          height: 20px;
          border-radius: 50%;
          background-color: $color-blue;
          color: $color-white;
          font-size: 8px;
          position: absolute;
          top: 18px;
          right: 15px;
          @include col-c-c;
          opacity: 0;
        }
      }
    }
    .right{
      height: 100%;
      display: flex;
      flex-direction: column;
      .r-left{
        ul{
          list-style: none;
          padding: 0;
          margin: 0;
          li:first-child{
            font-size: 12px;
            color: $color-blue-write;
            font-weight: bold;
            margin-bottom: 35px;
            pointer-events: none;
          }
          li{
            margin: 0 0 15px 20px;
            font-size: 14px;
            color: $color-grey-two;
            cursor: pointer;
            &:hover{
              color:$color-blue;
            }
          }
        }
      }
      .r-right{
        padding-left: 20px;
        .up{
          width: 100%;
          font-size: 12px;
          color: $color-blue-write;
          font-weight: bold;
        }
        .block-three{
          width: 100%;
          display: flex;
          margin-top: 15px;
          align-items: center;
          img{
            width: 50px;
            height: 50px;
            border-radius: 15px;
            margin-right: 20px;
          }
          div{
            width: 80%;
            font-size: 14px;
            color: $color-grey-two;
            cursor: pointer;
            &:hover{
              color:$color-blue;
            }
          }
        }
      }
    }
}
}
</style>
