<template>
    <div id="book-list-one">
        <h2>Book List One</h2>
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
    #book-list-one{
    background: rgb(218, 201, 14);
    box-shadow: 1px 2px 3px rgba(0,0,0,0.2);
    margin-bottom: 10px;
    padding: 10px 20px;
}
#book-list-one ul{
    padding: 0;
}
#book-list-one li{
    display: inline-block;
    margin-right: 10px;
    margin-top: 10px;
    padding: 20px;
    background: rgba(255,255,255,0.7);
}
.price{
    font-weight: bold;
    color: #E8800C;
}
</style>
