<template>
  <div>
    <Navbar/>
    <div class="main">
        <div class="main__one">
      <div class="main__one__card">
        <img src="/images/large.png" alt="" class="main__one__card__image">
      </div>
      
      <div class="main__one__text">
        <small><span class="main__one__text__frontend"><b>Front-End</b></span>  <img src="/images/dot.png" alt="dot" class="main__one__text__image"> <span class="main__one__text__hour">1 Hour Ago</span> </small>
        <h2 class="main__one__text__h2">Optimizing CSS for faster page loads</h2>
        <p class="main__one__text__p1">Not long ago I decided to improve the loading times of my website. It already loads pretty fast, but I knew there was still room for improvement and one of them was CSS loading. I will walk you through the process and show you how you can improve your load times as well.</p>
        <p class="main__one__text__p2">To see how CSS affects the load time of a webpage we first have to know how the browser converts an HTML document into a functional webpage...</p>
        
        <div class="main__one__text__footnote">
          <small class="main__one__text__footnote__small1">3 Min Read</small>
          <small class="main__one__text__footnote__small2"><a href="/details"><span class="main__one__text__footnote__small2__text"> Read Full</span>  &#8594;</a> </small>
        </div>
      </div>
    </div>
  
      
    <div class="main__two">
      <div class="main__two__card hover" v-for="(item, index) in blogposts " :key="index" @click="viewPost(item.id)">
        <div class="main__two__card__image">
          <img  :src="item.jetpack_featured_media_url" alt="css">
        </div>
        <div class="main__two__card__text ">
          <small><span class="main__one__text__frontend"><b>Front-End</b></span>  <img src="/images/dot.png" alt="dot" class="main__one__text__image"> <span class="main__one__text__hour">1 Month Ago</span> </small>
          <h2 class="main__one__text__h2">{{item.title.rendered }}</h2>
          <p class="main__one__text__p1">{{item.excerpt.rendered}}</p>
          <div class="main__one__text__footnote">
          <small class="main__one__text__footnote__small1">3 Min Read</small>
          <small class="main__one__text__footnote__small2"><span class="main__one__text__footnote__small2__text" > Read Full</span>  &#8594; </small>
        </div>
        </div>
      </div>
      <!-- <div class="main__two__card">
        <div class="main__two__card__image">
          <img src="/images/mini.png" alt="css">
        </div>
        <div class="main__two__card__text">
          <small><span class="main__one__text__frontend"><b>Front-End</b></span>  <img src="/images/dot.png" alt="dot" class="main__one__text__image"> <span class="main__one__text__hour">2 Months Ago</span> </small>
          <h2 class="main__one__text__h2">Colors in Css</h2>
          <p class="main__one__text__p1">Colors play a vital role in making a web page usable or not. In CSS, we can control the foreground and background color of an element with the color and background properties.</p>
          <div class="main__one__text__footnote">
          <small class="main__one__text__footnote__small1">3 Min Read</small>
          <small class="main__one__text__footnote__small2"><span class="main__one__text__footnote__small2__text">Read Full</span>  &#8594; </small>
        </div>
        </div>
      </div>
      <div class="main__two__card">
        <div class="main__two__card__image">
          <img src="/images/mini1.png" alt="css">
        </div>
        <div class="main__two__card__text">
          <small><span class="main__one__text__frontend"><b>Front-End</b></span>  <img src="/images/dot.png" alt="dot" class="main__one__text__image"> <span class="main__one__text__hour">2 Months Ago</span> </small>
          <h2 class="main__one__text__h2">Css Variables</h2>
          <p class="main__one__text__p1">CSS variables are custom properties that cascade normally and even inherit. They start with a reserved --- prefix, and there are no real rules about their value.</p>
          <div class="main__one__text__footnote">
          <small class="main__one__text__footnote__small1">3 Min Read</small>
          <small class="main__one__text__footnote__small2"><span class="main__one__text__footnote__small2__text">Read Full</span>  &#8594; </small>
        </div>
        </div>
      </div>
      <div class="main__two__card">
        <div class="main__two__card__image">
          <img src="/images/mini2.png" alt="css">
        </div>
        <div class="main__two__card__text">
          <small><span class="main__one__text__frontend"><b>Front-End</b></span>  <img src="/images/dot.png" alt="dot" class="main__one__text__image"> <span class="main__one__text__hour">1 Month Ago</span> </small>
          <h2 class="main__one__text__h2">Css Grid</h2>
          <p class="main__one__text__p1">The CSS Grid Layout Module offers a grid-based layout system, with rows and columns, making it easier to design web pages without having to use floats and positioning.</p>
          <div class="main__one__text__footnote">
          <small class="main__one__text__footnote__small1">3 Min Read</small>
          <small class="main__one__text__footnote__small2"><span class="main__one__text__footnote__small2__text">Read Full</span>  &#8594; </small>
        </div>
        </div>
      </div>
      <div class="main__two__card">
        <div class="main__two__card__image">
          <img src="/images/mini.png" alt="css">
        </div>
        <div class="main__two__card__text">
          <small><span class="main__one__text__frontend"><b>Front-End</b></span>  <img src="/images/dot.png" alt="dot" class="main__one__text__image"> <span class="main__one__text__hour">2 Months Ago</span> </small>
          <h2 class="main__one__text__h2">Colors in Css</h2>
          <p class="main__one__text__p1">Colors play a vital role in making a web page usable or not. In CSS, we can control the foreground and background color of an element with the color and background properties.</p>
          <div class="main__one__text__footnote">
          <small class="main__one__text__footnote__small1">3 Min Read</small>
          <small class="main__one__text__footnote__small2"><span class="main__one__text__footnote__small2__text">Read Full</span>  &#8594; </small>
        </div>
        </div>
      </div>
      <div class="main__two__card">
        <div class="main__two__card__image">
          <img src="/images/mini1.png" alt="css">
        </div>
        <div class="main__two__card__text">
          <small><span class="main__one__text__frontend"><b>Front-End</b></span>  <img src="/images/dot.png" alt="dot" class="main__one__text__image"> <span class="main__one__text__hour">2 Months Ago</span> </small>
          <h2 class="main__one__text__h2">Css Variables</h2>
          <p class="main__one__text__p1">CSS variables are custom properties that cascade normally and even inherit. They start with a reserved --- prefix, and there are no real rules about their value.</p>
          <div class="main__one__text__footnote">
          <small class="main__one__text__footnote__small1">3 Min Read</small>
          <small class="main__one__text__footnote__small2"><span class="main__one__text__footnote__small2__text">Read Full</span>  &#8594; </small>
        </div>
        </div>
      </div> -->
    </div>
    <div class="main__three">
      <h2 class="main__three__h2">Join our team of writers</h2>
      <p class="main__three__p">On dasdas, writers earn a living doing what they love. 
Getting started is easy. Just pay a one time $25 fee and everything is ready to go.</p>
    <button @click="payViaService" class="main__three__button">Join Us</button>
    </div>
    </div>
  </div>
</template>

<script>
import {FlutterwavePayButton} from "flutterwave-vue-v3"
export default {
  name: 'IndexPage',
  components:{
     FlutterwavePayButton
  },
  data(){
    return{
      blogposts: {},
      paymentData: {
        tx_ref: this.generateReference(),
        amount: 25,
        currency: 'USD',
        payment_options: 'card',
        redirect_url: '',
        meta: {
          'counsumer_id': '7898',
          'consumer_mac': 'kjs9s8ss7dd'
        },
        customer: {
          name: 'Demo Customer  Name',
          email: 'customer@mail.com',
          phone_number: '081845***044'
        } ,
        customizations: {
          title: 'Customization Title',
          description: 'Customization Description',
          logo: 'https://flutterwave.com/images/logo-colored.svg'
        },
        callback: this.makePaymentCallback,
        onclose: this.closedPaymentModal
      }
    }
  },
  mounted(){
    this.getPosts()
  },
  methods:{
    getPosts(){
      this.$axios.get( "https://techcrunch.com/wp-json/wp/v2/posts")
        .then((response) => {
          this.blogposts = response.data;
          console.log(this.blogposts)
          
        });
    },
    payViaService() {
      this.payWithFlutterwave(this.paymentData) 
    } ,
    makePaymentCallback(response) {
      console.log("Pay", response)
    },
    closedPaymentModal() {
      console.log('payment is closed');
    },
    generateReference(){
      let date = new Date()
      return date.getTime().toString();
    },
    viewPost(post) {
      this.$router.push(`/${post}`);
    },
  }
}
</script>

<style scoped>
@font-face {
  font-family: "SFmedium";
  src: local("SFmedium"),
  url(../static/fonts/SFPRODISPLAYREGULAR.OTF) format("truetype");
}
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  font-family: "SFmedium";
}
.main{
  padding: 0px 158px;
}
.hover:hover{
  cursor: pointer;
}
.main__one{
  background: #FFFFFF;
  border: 1px solid #F5F5F5;
  border-radius: 5px;
  display: grid;
  grid-template-columns: 1fr 1fr;
  column-gap: 16px;
}
.main__one__card{
  padding: 8px;
}
.main__one__card__image{
  width: 100%;
  height: 100%;
}
.main__one__text{
  padding: 8px;
}
.main__one__text__hour{
  color: #6E6E6E;
  margin-left: 4px;
  display: inline-block;
}
.main__one__text__frontend{
  color: #4B4B4B;
  margin-right: 4px;
  margin-top: 12px;
  display: inline-block;
}
.main__one__text__h2{
  font-weight: 900;
  font-size: 22px;
  line-height: 26px;
  color: #2C2C2C;
  padding-bottom: 8px;
}
.main__one__text__p1{
  font-weight: 400;
  font-size: 14px;
  line-height: 21px;
  color: #6E6E6E;
  margin-bottom: 1rem;
}
.main__one__text__p2{
  font-weight: 400;
  font-size: 14px;
  line-height: 21px;
  color: #6E6E6E;
}
.main__one__text__footnote{
  display: grid;
  grid-template-columns: 1fr 1fr;
  margin-top: 20px;
}
.main__one__text__footnote__small1{
  font-weight: 500;
  font-size: 12px;
  line-height: 14px;
  color: #6E6E6E;
}
.main__one__text__footnote__small2{
  font-weight: 700;
  font-size: 12px;
  line-height: 14px;
  color: #1473E6 !important;
  text-decoration: none !important;
}
a{
  color: #1473E6 !important;
  text-decoration: none !important;
}

.main__one__text__footnote__small2{
  display: inline-block;
  text-align: right;
  text-decoration: none !important;
}
.main__two{
  margin-top: 52px;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  column-gap: 47px;
  row-gap: 48px;
}
.main__two__card{
  border: 1px solid #F5F5F5;
  border-radius: 5px;
  padding: 10px;
}
.main__two__card__image img{
  width: 100%;
}
.main__three{
  margin-top: 156px;
  text-align: center;
  width: 600px;
  margin-left: auto;
  margin-right: auto;
}
.main__three__h2{
  font-weight: 500;
  font-size: 32px;
  line-height: 38px;
  color: #2C2C2C;
  margin-bottom: 12px;
}
.main__three__p{
  font-weight: 400;
  font-size: 22px;
  line-height: 32px;
  color: #6E6E6E;
  margin-bottom: 35px;
}
.main__three__button{
  padding: 12px 55px;
  background: #000000;
  color: white;
  margin-bottom: 227px;
  border: none;
}

@media(max-width:576px){
  .main{
  padding: 0px 10px;
}
  .main__one{
  background: #FFFFFF;
  border: 1px solid #F5F5F5;
  border-radius: 5px;
  display: grid;
  grid-template-columns: 1fr;
  column-gap: 16px;
}
  .main__one__text__h2{
  font-weight: 900;
  font-size: 22px;
  line-height: 26px;
  color: #2C2C2C;
  padding-bottom: 12px;
  padding-top: 12px;
}
  .main__two{
  margin-top: 52px;
  display: grid;
  grid-template-columns: 1fr;
  column-gap: 47px;
  row-gap: 30px;
}
.main__three{
  margin-top: 100px;
  text-align: center;
  width: 100%;
  margin-left: auto;
  margin-right: auto;
}
}


@media(min-width:577px) and (max-width:768px){
  .main{
  padding: 0px 10px;
}
  .main__one{
  background: #FFFFFF;
  border: 1px solid #F5F5F5;
  border-radius: 5px;
  display: grid;
  grid-template-columns:1fr;
  column-gap: 8px;
  
}
.main__two{
  margin-top: 52px;
  display: grid;
  grid-template-columns: 1fr 1fr;
  column-gap: 30px;
  row-gap: 30px;
}
}

@media(min-width:769px) and (max-width:1200px){
  .main{
  padding: 0px 10px;
}
  .main__one{
  background: #FFFFFF;
  border: 1px solid #F5F5F5;
  border-radius: 5px;
  display: grid;
  grid-template-columns: 1fr 1fr;
  column-gap: 8px;
}

}
</style>
