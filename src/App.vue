<template>
    <div id="app">
        <compBookListOne ></compBookListOne>
        <compBookListTwo ></compBookListTwo>
        <button class="btn btn-success" @click="reducePrice">Reduce Price</button>
    </div>
</template>

<script>
import {mapActions} from 'vuex'
import compBookListOne from "./components/BookListOne"
import compBookListTwo from "./components/BookListTwo"
export default {
    
    components:{
      compBookListOne,
      compBookListTwo
    },
    methods:{
        ...mapActions([
            'reducePrice'
        ])
    }
}
</script>
