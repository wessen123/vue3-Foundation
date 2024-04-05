<script setup>
import {ref} from "vue"
import quizes from "../data/quizes.json"

import {defineProps} from "vue"

    const props= defineProps(['newquiz'])

 const count =ref(0)
 const increment=ref(10)
</script>
<template>
    
    <div>
        <h1>{{ count }} </h1>
        <button @click="count+=increment">+</button>
        <button  @click="count--">-</button>
        <ul v-for="q in quizes">
          <li>{{q.name}}</li>    
        </ul>
    </div>
    <pre>{{props}}</pre>

</template>

<style scoped>
button-1{
    color:blue;
    padding: 100px;
    background-color: aqua;

}
h1{

    color: red;
}
li{
    display: block;
}
</style>