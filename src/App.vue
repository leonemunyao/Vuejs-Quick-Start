<script setup>
  import { reactive, ref } from 'vue'

  const counter = reactive({ count: 1 })
  const message = ref('I am Leon')
</script>

<template>
   <div class="main">
    <h1>{{ message }}</h1>
    <p class="myname">The count is {{ counter.count }}</p>
    <div class="blog">
     <h2>The Application Instance</h2>
     <p>Every Vue application starts by creating a new application instance with the createAPP function.
       exmple, <br><ul>
                   <li>
                     import { createApp } from 'vue'
 
                     const app = createApp({
                       <em>root component options</em>
                     })
                   </li>
               </ul>
     </p>
      <br>
     <h2>The Root Component</h2>
     <p>The object we are passing in create app is infact a component. When using SFC we typically import 
       the root components from another file. example, <br>
       <ul>
         <li>
             import { createApp } from 'vue'
 
             import { App } from './App.vue'
             const app = createApp(App)
         </li>
       </ul>
     </p>
    </div>
   </div>
</template>

<style scoped>

</style>
