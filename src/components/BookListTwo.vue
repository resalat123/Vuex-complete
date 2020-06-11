<template>
    <div id="book-list-two">
        <h2>Book List Two</h2>
        <ul>
             <li v-for="(b,id) in saleBooks" :key="id">
                <span class="name">{{b.name}}</span>
                <span class="price">${{b.price}}</span>
            </li>
        </ul>
    </div>
</template>

<script>
import {mapGetters} from 'vuex'
export default {
    computed:{
      book(){
          return this.$store.state.books;
      },
      ...mapGetters([
          'saleBooks'
      ])
   }
}
</script>

<style scoped>
    #book-list-two{
    background: rgb(46, 102, 180);
    box-shadow: 1px 2px 3px rgba(0,0,0,0.2);
    margin-bottom: 30px;
    padding: 10px 20px;
}
#book-list-two ul{
    padding: 0;
    list-style-type: none;
}
#book-list-two li{
    margin-right: 10px;
    margin-top: 10px;
    padding: 20px;
    background: rgba(255,255,255,0.7);
}
.price{
    font-weight: bold;
    color: rgb(12, 126, 232);
    display: block;
}
</style>
