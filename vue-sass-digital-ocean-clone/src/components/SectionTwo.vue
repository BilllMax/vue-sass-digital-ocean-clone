<template>

<div class="container-review">

  <div class="center-container">
    <img :src="data.logo" alt="">
  </div>

  <p class="text">
    As a founder and somebody that doesn't have a DevOps <br>
    background, I didn't spend every morning of my life wearing a pager <br>
    and doing XML sit-ups…what I wanted to <br> 
    do was ship an application to users so that we could begin iterating it
  </p>

  <p class="name">{{data.name}}</p>

  <p class="role">{{data.role}}</p>
  

</div>

</template>

<script>
const data = 
{
  logo:"https://www-static.cdn.prismic.io/www-static/51b30313-4461-4791-9dae-edad80d4ece6_parabol_logo.svg",
  name:"Jordan Husney",
  role:"Cofounder & CEO of Parabol"
}
export default {
  name: 'SectionTwo',
  props: {
    msg: String
  },
  data() {
    return {
      data
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../../public/style/positions.scss';
@import '../../public/style/color.scss';
@import '../../public/style/ui.scss';

.container-review{
  height: 55vh;
  background-color: $color-sec2-back;
  padding: 0 10px;
  @include col-c-c;
  .center-container{
    img{
      height: 40px;
      width: 200px;
    }
  }
  p{
    text-align: center;
    color: $color-white;
  }
  .text{
    font-size: 24px;
    margin: 25px 0;
    font-weight: 200;
  }
  .name{
    margin-bottom: 15px;
  }
  .role{
    font-size: 15px;
  }

}
</style>