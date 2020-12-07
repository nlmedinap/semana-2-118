<template>
    <div class="row mt-md-5 mt-sm-5 mt-xs-5">
  <div class="col-lg-6 col-xs-12" v-for="(news, index) of news" :key="index">

    <div class="d-flex justify-content-center align-items-center">
      <div class="p-3">
        <img :src="news.urlToImage" alt="new urlToImage" width="100%" height="100%"> 
      </div>
      <div class="p-2">
          <h4>{{news.title}}</h4>
          <hr>

          <h6> {{news.description}} </h6>

      </div>
    </div>
    <div class="d-flex container-fluid justify-content-end pb-2 mt-n2">
      <a :href="news.url" class="btn btn-outline-info">Info</a>
    </div>
  </div>
</div>
</template>

<script>
import axios from "axios";

export default {
    name: 'SectionApi',
    data(){
        return{
            news: null
        }
    },
    mounted(){
    axios
    .get("http://newsapi.org/v2/top-headlines?country=co&apiKey=ca74aeb15fc0497aa035c63b45532356")
    .then((response)=>{
        (this.news=response.data.articles.slice(0,4))
        console.log(this.news)
    })

    }
}
</script>
<style scoped>

</style>