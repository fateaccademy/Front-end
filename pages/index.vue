<template>
  <section>
   <!--<Header/>-->

    <div>
      <h1>Posts</h1>
    </div>
    <div class="posts">
      <nuxt-link :to="'/posts/'+post.id" class="post" v-for="post in posts" :key="post.id">
        <div class="bg" :style="{ background: 'url('+post.img+')'}"></div>
        <p>{{post.title}}</p>
      </nuxt-link>
    </div>


  </section>

</template>

<script>
import Header from "../components/Header";
export default {
  components: {
    Header
  },
  data(){
    return {
      posts:[
        {id:1,title:"re1",img:'https://images.unsplash.com/photo-1551122560-c4bed8cdcc15?ixlib=rb-1.2.1&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=1080&fit=max&ixid=eyJhcHBfaWQiOjE5Mzk5fQ'},
        {id:2,title:"re2",img:'https://images.unsplash.com/photo-1551092868-0b77c6db2537?ixlib=rb-1.2.1&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=1080&fit=max&ixid=eyJhcHBfaWQiOjE5Mzk5fQ'},
        {id:3,title:"re3",img:'https://images.unsplash.com/photo-1551103124-78b59627166e?ixlib=rb-1.2.1&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=1080&fit=max&ixid=eyJhcHBfaWQiOjE5Mzk5fQ'},
        {id:4,title:'qw',img:'https://images.unsplash.com/photo-1542834281-979df8f0a97b?ixlib=rb-1.2.1&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=1080&fit=max&ixid=eyJhcHBfaWQiOjE5Mzk5fQ'}
      ]
    }
  }
}
</script>

<style scoped>
  .posts{
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
  }

  .post{
    border: 1px solid;
    width: 30%;
    height: 30vh;
    margin: 10px 0;
  }
  .post .bg{
    background-position: center!important;
    background-size: cover!important;
    background-repeat: no-repeat!important;
    width: 100%;
    height: 100%;
  }
  
  @media (max-width: 786px) {
    .post{
      width: 45%;
    }
  }

  @media (max-width: 375px) {
    .post{
      width:100%;
    }
  }
</style>

