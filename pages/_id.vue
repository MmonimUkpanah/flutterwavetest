<template>
  <div>
    <Navbar/>
    <div class="main">
        <div class="main__one">
            <small><span class="main__one__boldspan"><b>By Ryan Jackson</b></span> <span class="main__one__lightspan">2 Months Ago</span></small>
            <h2 class="main__one__h2">{{post.title.rendered}}</h2>
            <p class="main__one__firstp">{{post.excerpt.rendered}}</p>
            <div class="main__one__imagecontainer">
                <img :src="post.jetpack_featured_media_url" class="main__one__image" alt="">
            </div>
            <p class="main__one__secondp">{{post.content.rendered}}</p>
        </div>
        <div class="main__two__sub">
            <h2 class="main__two__sub__h2">More Articles</h2>
            <div class="main__two">
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
          <small class="main__one__text__footnote__small2"><span class="main__one__text__footnote__small2__text" style="cursor:pointer">Read Full</span>  &#8594; </small>
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
      </div>
      
    </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
    data(){
        return{
          post:{}

        }
    },
    mounted(){
        this.getPost()
    },
    methods:{
        async getPost() {
      try {
        const response = await this.$axios.get(
          `https://techcrunch.com/wp-json/wp/v2/posts/${this.$route.params.id}`
        );
        
        this.post = response.data;
        console.log(this.post)
        
      } catch (error) {
        console.error(error);
        
      }
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
.main__one__text__footnote__small2__text:hover{
    cursor: pointer;
}
.main__one{
    margin-top: 60px;
    width: 714px;
    margin-left: auto;
    margin-right: auto;
}
.main__one__boldspan{
    font-weight: 500;
font-size: 12px;
line-height: 14px;
color: #4B4B4B;
}
.main__one__lightspan{
    font-weight: 500;
    font-size: 12px;
    line-height: 14px;
    color: #6E6E6E;
}
.main__one__h2{
    font-weight: 900;
    font-size: 32px;
    line-height: 38px;
    color: #2C2C2C;
    margin-top: 10px;
}
.main__one__firstp{
    font-weight: 400;
    font-size: 14px;
    line-height: 21px;
    color: #6E6E6E;
    margin-top: 23px;
}
.main__one__image{
    width: 510px;
    height: 327px;
    margin-left: auto;
    margin-right: auto;
    display: block;
    margin-top: 40px;
    margin-bottom: 40px;
}
.main__one__secondp{
    font-weight: 400;
    font-size: 14px;
    line-height: 21px;
    color: #6E6E6E;
    margin-bottom: 20px;
}
.main__one__thirdp{
    font-weight: 400;
    font-size: 14px;
    line-height: 21px;
    color: #6E6E6E;
}
.main__two__sub{
    margin-top: 50px;
    margin-bottom: 200px;
}
.main__two__sub__h2{
    font-weight: 900;
    font-size: 24px;
    line-height: 29px;
    color: #2C2C2C;
}
.main__two{
  margin-top: 23px;
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
  color: #1473E6;
  cursor: pointer;
}

.main__one__text__footnote__small2{
  display: inline-block;
  text-align: right;
}

@media(max-width:576px){
    .main{
  padding: 0px 10px;
}
    .main__one{
    margin-top: 60px;
    width: 100%;
    margin-left: auto;
    margin-right: auto;
}
    .main__one__image{
    width: 100%;
    height: auto;
    margin-left: auto;
    margin-right: auto;
    display: block;
    margin-top: 40px;
    margin-bottom: 40px;
}
 .main__two{
  margin-top: 23px;
  display: grid;
  grid-template-columns: 1fr;
  column-gap: 47px;
  row-gap: 30px;
}
}


@media(min-width:577px) and (max-width:1200px){
    .main{
  padding: 0px 20px;
} 
}

</style>