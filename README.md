<!DOCTYPE html>
<html>
<script src="https://cdn.jsdelivr.net/npm/vue"></script>
<script src="js/vue-jquery.js"></script>
<body>
<header>
<div id="top-header">
<img bind:src="'/images/logo.png'">
</div>
<div id="navigation">
<ul>
    <li v-for="x in todos">
       {{x.text}}
   </li>
</ul>
</div>
</header>

<div id="app">
  <h1>{{ message }}</h1>
</div>

<script>
var myMenu = new Vue({
 el: '#navigation',
 data: {
 todos:[
 { text: 'Home'},
 { text: 'About us'},
 { text: 'Blog'},
 { text: 'Contact Us'}
 ]
 }
})
var myObject = new Vue({
  el: '#app',
  data: {message: 'Hello Vue!'}
})
</script>

</body>
</html>
