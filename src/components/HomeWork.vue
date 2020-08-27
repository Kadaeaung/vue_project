<template>
  <div>
    <h2 class="text-danger">Homework Component</h2>
    
    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <div class="card mb-3" v-for="(article,i) in info" :key="i">
            <div class="row no-gutters">
              <div class="col-md-4">
                <img :src="article.urlToImage" class="card-img" alt="...">
              </div>
              <div class="col-md-8">
                <div class="card-body">
                  <h5 class="card-title">{{article.title}}</h5>
                  <p class="card-text">{{article.description}}</p>
                  <p class="card-text"><small class="text-muted">Last updated 3 mins ago</small></p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
      
        

  </div>
</template>

<script type="text/javascript">
  export default {
    name: 'Testing',
    data(){
      return {
        loading: true,
        error: false,
        info: null
      }
    },
    mounted(){
      this.getData();
    },
    methods:{
      getData(){
        this.$http.get('http://newsapi.org/v2/top-headlines?sources=techcrunch&apiKey=f0c75f2f0ee6442889dac7ec98605b6e')
                .then(res=>{
                  console.log(res);
                  this.info = res.data.articles;
                })
                .catch(err=>{
                  this.error = true;
                  console.log(err);
                })
                .finally(()=>{
                  this.loading = false;
                })
      }
    }
  }
</script>

<style type="text/css">
  
</style>