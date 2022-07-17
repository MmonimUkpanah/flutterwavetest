<template>
  <div class="navbar">
    <div class="navbar__logo">
        <img src="/images/logo.png" alt="logo" class="navbar__logo__image">
    </div>
    <div class="navbar__icons">
        <img src="/images/vector.png" alt="twitter" class="navbar__icons__twitter">
        <img src="/images/dot.png" alt="dot" class="navbar__icons__dot">
        <img src="/images/dribbble.png" alt="dribble" class="navbar__icons__dribble">
        <img src="/images/dot.png" alt="dot" class="navbar__icons__dot">
        <img src="/images/figma.png" alt="figma" class="navbar__icons__figma">
        <img src="/images/dot.png" alt="dot" class="navbar__icons__dot">
        <img src="/images/github.png" alt="github" class="navbar__icons__github">
    </div>
  </div>
</template>

<script>
export default {

}
</script>


<style scoped>
    *{
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }
    .navbar{
        padding: 10px 158px;
        display: grid;
        grid-template-columns: 1fr 1fr;
    }
    .navbar__logo__image{
        width: 80px;
        height: 80px;
    }
    .navbar__icons{
        display: grid;
        grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr 1fr;
        text-align: right;
        padding-top: 36px;
        padding-bottom: 36px;
        padding-left: 18rem;
    }
    .navbar__icons__dot{
        width: 4px;
        padding-top: 10px;
        padding-bottom: 10px;
    }
    .navbar__icons__twitter,
     .navbar__icons__dribble,
     .navbar__icons__figma,
     .navbar__icons__github{
        height: 24px;
        width: 24px;
        
     }


     @media(max-width:576px) {
        .navbar{
        padding: 10px 10px;
        display: grid;
        grid-template-columns: 1fr 1fr;
        }
        .navbar__icons{
        display: grid;
        grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr 1fr;
        text-align: left;
        padding-top: 30px;
        padding-bottom: 30px;
        padding-left: 0;
    }
     }


     @media(min-width:577px) and (max-width:1200px){
        .navbar{
        padding: 10px 20px;
        display: grid;
        grid-template-columns: 1fr 1fr;
        }
        .navbar__icons{
        display: grid;
        grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr 1fr;
        text-align: left;
        padding-top: 30px;
        padding-bottom: 30px;
        padding-left: 0;
    }
     }
</style>