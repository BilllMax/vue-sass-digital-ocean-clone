<template>
<nav>

    <div class="jumbo">
        <div class="content-container">
            <div class="jumbo-text">
                <div class="center-container">
                    <h2>{{jumboText.title}}</h2>
                    <div class="paragraph" v-html="jumboText.body"></div>
                <span>
                    <img src="../assets/img/play.svg" alt="">
                    <small>{{jumboText.subtitle}}</small>
                </span>
                </div>
            </div>
            <div class="jumbo-form">

                <div class="form">

                    <div class="head">
                        <h3>{{form.header}}</h3>
                    </div>

                    <div class="input-container">
                      <input type="text" placeholder="First Name">
                      <input type="text" placeholder="Email Address">
                      <input type="text" placeholder="Password">
                      <div class="btn-blue">
                          <p class="txt">Sign up with email</p>
                      </div>
                    </div>

                    <hr>

                    <div class="bottom">

                        <div class="btn-container">
                        <span class="btn-google">
                            <i class="fab fa-google"></i>
                            {{form.google}}
                        </span>
                        <span class="btn-git">
                            <i class="fab fa-github"></i>
                        </span>
                        </div>
                        
                    </div>

                </div>

            </div>
        </div>
    </div>

</nav>

</template>

<script>
// import '../../public/positions.scss'
const jumboText =
{
    title: 'Simplicity at work',
    body: 'Get everything your development <br> teams need to succeed.',
    subtitle: 'Hear from our customers(1:58)'
}

const form =
{
    header:'Deploy in seconds',
    email: 'Sign up with email',
    google: 'Sign up with Google',
}


export default {
  name: 'Jumbo',
  props: {
    msg: String
  },
  data() {
      return {
          jumboText,
          form
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../../public/style/positions.scss';
@import '../../public/style/color.scss';
@import '../../public/style/ui.scss';

.jumbo{
  height: 80vh;
  background-image: url("https://www.digitalocean.com/static/bg-home-hero-3-bb4b33b77274db09b969f629ad81c4d5.svg");
  background-size: cover;
  margin-top: 100px;
  @media screen and (min-width: 890px) and (max-width: 1200px) {
      height: 80vh;
      margin-top: 0px;
  }
  @media screen and (min-width: 769px) and (max-width: 890px) {
      height: 80vh;
      margin-top: 0px;
  }
  @media screen and (min-width: 360px) and (max-width: 768px) {
      height: 130vh;
      margin-top: 0px;
  }
  @include col-c-c;
  .content-container{
      width: 864px;
      height: 65vh;
      min-height: 475px;
      display: flex;
      @media screen and (min-width: 360px) and (max-width: 768px) {
          flex-direction: column;
          justify-content: center;
          align-items: center;
          height: 130vh;
      }
      .jumbo-text{
          min-width: 432px;
          @include col-c;
          color: $color-white;
        .center-container{
            margin-top:120px;
            @media screen and (min-width: 360px) and (max-width: 768px) {
            margin-top: 0;
            }
          h2{
           color: $color-white;
           font-size: 45px;
             @media screen and (min-width: 360px) and (max-width: 768px) {
                 font-size: 30px;
                 text-align: center;
            }
            }
            .paragraph{
              font-size: 25px;
              margin: 25px 0;
            @media screen and (min-width: 360px) and (max-width: 768px) {
                 font-size: 20px;
                 text-align: center;
            }
            }
          span{
          @include row-c;
          cursor: pointer;
            @media screen and (min-width: 360px) and (max-width: 768px) {
            margin-left: 50px;
            }
            small{
                margin-left: 10px;
            }
          }
        }
      }
      .jumbo-form{
          min-width: 432px;
          @include col-c-c;
          .form{
              background-color: $color-white;
              height: 530px;
              width: 340px;
              border-radius: 10px;
              @media screen and (min-width: 360px) and (max-width: 768px) {
              margin-top: 25px;
            }
              .head{
                  border-radius: 10px;
                  background-color: $color-grey;
                  height: 53px;
                  width: 340px;
                  margin-bottom: 30px;
                  @include col-c-c;
                  h3{
                    color:$color-blue-write;
                  }
              }
              .input-container{
                  @include col-c-c;
                  width: 100%;
                  input{
                      padding: 15px;
                      width: 70%;
                      margin-bottom: 10px;
                      font-size: 18px;
                  }
                  input:focus{
                    border:none;
                    outline-color: $color-blue;
                  }
                  .btn-blue{
                      @include btn-blue;
                      color: $color-white;
                      width: calc(70% + 30px);
                      cursor: pointer;
                      .txt{
                        font-weight: 900;
                        font-size: 18px;
                      }
                  }
                  .btn-blue:hover{
                      background-color: $color-blue-hover;
                  }
              }
              hr{
                border:0.2px solid $color-grey;
                margin: 30px 0;
              }
              .bottom{
                  display: flex;
                  flex-direction: column;
                  justify-content: center;
                  align-items: center;
                .btn-container{
                    width: calc(70% + 30px);
                    display: flex;
                    flex-direction: row;
                    justify-content: space-between;
                   .btn-google{
                    height: 60px;
                    line-height: 60px;
                    width: 70%;
                    border-radius: 5px;
                    display: inline-block;
                    text-align: center;
                    background-color: $color-white;
                    border: 1px solid $color-blue;
                    color: $color-blue;
                    cursor: pointer;
                   }
                   .btn-git{
                    height: 60px;
                    line-height: 60px;
                    width: 20%;
                    border-radius: 5px;
                    display: inline-block;
                    text-align: center;
                    background-color: $color-white;
                    border: 1px solid $color-blue;
                    color: $color-blue;
                    cursor: pointer;
                   }
                }
              }
          }
      }
  }
}
</style>