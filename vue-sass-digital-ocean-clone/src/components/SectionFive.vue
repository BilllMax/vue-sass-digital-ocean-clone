<template>

<div class="container-started">

  <div class="container">
    <h2>Ready to get started?</h2>

    <div class="btn-container">
      <div class="btn-sec-five transparent"><p class="txt">Talk to an expert</p></div>
      <div class="btn-sec-five white"><p class="txt">Start your free trial</p></div>
    </div>
  </div>

</div>

</template>

<script>
export default {
  name: 'SectionFive',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../../public/style/positions.scss';
@import '../../public/style/color.scss';
@import '../../public/style/ui.scss';

.container-started{
  height: 190px;
  background: url("https://images.prismic.io/www-static/3feed7b8-c2d5-4cbb-95c8-ecc177ae05f9_contact-bg.jpeg?auto=compress,format");
  background-size: cover;
  background-position: 20% 50%;
  @include col-c-c;
  @media screen and (min-width: 360px) and (max-width: 839px) {
    height: 370px;
  }

  @media screen and (min-width: 840px) and (max-width: 1023px) {
    height: 298px;
  }
  
  @media screen and (min-width: 1024px) and (max-width: 1215px) {
    height: 256px;
  }

  .container{
    width: 95%;
    @include row-sb-c;
    justify-content: space-around;
    @media screen and (min-width: 360px) and (max-width: 839px) {
          // below 839 column / column
          flex-direction: column;
          align-items: center;
          text-align: center;
    }

    @media screen and (min-width: 840px) and (max-width: 1023px) {
          // 840-1023 column / row
          flex-direction: column;
    }

    @media screen and (min-width: 1024px) and (max-width: 1215px) {
          // 1024-1215 inline / column
          flex-direction: row;
    }


    h2{
      color: $color-white;
      font-size: 36px;
      font-weight: 600;
    }
    .btn-container{
      @include row-sb-c;
      justify-content: space-around;
      width: 550px;
    @media screen and (min-width: 360px) and (max-width: 839px) {
          // below 839 column / column
          flex-direction: column;
    }

    @media screen and (min-width: 840px) and (max-width: 1023px) {
          // 840-1023 column / row
          flex-direction: row;
          margin: 30px auto;
    }

    @media screen and (min-width: 1024px) and (max-width: 1215px) {
          // 1024-1215 inline / column
          flex-direction: column;
          justify-content: space-between;
    }

// below 839 column / column
// 840-1023 column / row
// 1024-1215 inline / column
// da 1216 in sù  inline / inline

      .btn-sec-five{
        // @include btn-sec-five;
        height: 60px;
        line-height: 60px;
        width: 210px;
        border-radius: 5px;
        display: inline-block;
        text-align: center;
        padding: 0;
        cursor: pointer;
        @media screen and (min-width: 360px) and (max-width: 839px) {
              // below 839 column / column
              margin-top: 30px;
        }
          @media screen and (min-width: 1024px) and (max-width: 1215px) {
          margin: 10px auto;
        }

        .txt{
          font-size: 16px;
          font-weight: 600;
          max-width: 210px;
        }
      }
      .transparent{
        border: 1px solid $color-white;
        color: $color-white;
      }
      .transparent:hover{
        background-color: rgba($color: #fff, $alpha: 0.2);
      }
      .white{
        background-color: $color-white;
        color: $color-blue;
      }
      .white:hover{
        opacity: 0.8;
      }
    }
  }
}
</style>