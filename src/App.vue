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
       <br>
        While many examples in this guide only need a single component,
        most real applications are organized into a tree of nested, reusable components. 
        For example, a Todo application's component tree might look like this:
        <ul>
          <li>
            App (root component)
       1.TodoList
           TodoItem
              TodoDeleteButton
              TodoEditButton
        2.TodoFooter
           TodoClearButton
           TodoStatistics
          </li>
        </ul>
     </p>
     <br>
     <h2>Mounting the App</h2>
     <p>
       An application won't render anything until its .mount() its called.
       It expects a "container" argment which can either be an actual DOM element
       or a selector string, example 
        <ul>
          <li>
            div id="app" div
            <br>
            app.mount('#app')
          </li>
        </ul>
     </p>
     <h2>In-DOM Root Component</h2>
     <p>The template for the root element is usually part of the component
      
     </p>
    </div>
   </div>
</template>

<style scoped>
  .main {
    text-align: center;
    margin: 20px;
  }

  h1 {
    font-size: 24px;
    color: #333;
    margin-bottom: 10px;
  }

  .myname {
    font-size: 18px;
    color: #242222;
    margin-bottom: 20px;
  }

  .blog {
    background-color: #f5f5f5;
    padding: 20px;
    border-radius: 5px;
    margin-top: 20px;
  }

  h2 {
    font-size: 20px;
    color: #555;
    margin-bottom: 10px;
  }

  p {
    font-size: 16px;
    color: #777;
    margin-bottom: 10px;
  }

  ul {
    list-style-type: square;
    margin-left: 20px;
  }

  li {
    margin-bottom: 5px;
  }
</style>
