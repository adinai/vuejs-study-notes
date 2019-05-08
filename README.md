
# Vue Js Study Notes 
# Day 1 

### Vue Instance {{  }}
Every Vue application starts by creating a new Vue instance with Vue function:
```javascript
var vm = new Vue({
//options
})
```
```javascript
{{product +'?'}}
{{ firstName + ' '+ lastName}}
{{ clicked ? true : false}}
{{message.split('').reverse().join('')}}
```

### Conditional Directives with Vue.js
**The ability to show or hide elements based on conditions is a fundamental feature of any frontend framework. Vue.js provides us with a set of core directives to achieve this effect: v-if, v-else, v-else-if and v-show.**

The **v-if** directives adds or removes DOM elements based on the given expression.
```javascript
data(){
return {
msg: "Vuejs Learning",
isLoggedIn: false
}}

------------
<button v-if="isLoggedIn">Logout</button>
```
Now,the button will not show beacuse **isLoggedIn** is set to false,but if we set **isLoggedIn** to true, it will add the button to DOM.

⋅⋅* To control multiple elements with a single **v-if** we should put them into **<template>** element as follows.
 ```javascript
 <template v-if="isLoggesIn">
  <label> Logout </button>
  <button> Logout </button>
 </template>
 ```
 
 **Login // Logout buttons ---- v-else----**
 ```javascript
 <button v-if="isLoggedin">Logout</nutton>
 <buttin v-else>Login </button>
 ```
 **v-else-if** can be used when we need more than two options to be checked. This will ensure that only one of the chained items in the else-if chain will be visible.

For example, if the property named isLoginDisabled is true, we can prevent the Log In button from displaying and instead display a label. We can accomplish it by using the v-else-if directive as follows.
 ``` javascript
 <button v-if="isLoggedIn>Logout</button>
 <label v-else-if="isLoginDisabled">Register Disabled </label>
 <button v-else> Login</button>
 ```
 Very similar to v-if, the v-show directive can also be used to show and hide an element based on an expression.
 
 ### v-for - Rendering list of items 
 ```javascript
 data(){
 return{
 messages: ['hi', 'hello', 'bye'],
 shoppingItems: [
 {name: 'apple', price: '10'},
 {name: 'orange', price:'20'}
 ]
 }
 }
 



### Directives
In Vue, two-way binding is accomplished using the **v-model** directives.
It can be used well with Binding to Checkboxes and Radio Buttons 
```javascript
<div id="app">
<h1>{{message}}</h1>
<input type="text" v-model="message" />
</div>

<script>
var app = new Vue({
el: '#app'
data:{
message:'Hello'
}
})
</script>
```

### Events 

 
 




### Documentation
The [docs](https://drive.google.com/drive/folders/1Wh669MzW5aWhxuzNXWnG3CLZJ-KyRKyM?usp=sharing) is available in the google drive which can access. :gift: We would be happy if you contribute to write GitHub pages docs for this.


### Follow me on Twitter
[Follow me on Twitter](https://twitter.com/badarshahzad54/status/859596238202691584)




### Features

+ Browse the Web.
+ Manage **History** of browsing.
+ Keep your favourite sites saved in **Bookmarks**.
+ Download files with our browser's **Downloader**.
+ Convert HTML page into PDF with our **HTML to PDF converter** and save it to your local machine.
+ Keep your *secret* online accounts saved in **Passowrd Valut**.

### Usage

+ Once you have all Dependencies.
+ download the project or clone it [click here](https://github.com/badarshahzad/Jfx-Browser/tree/master)
+ open the SEGP folder with your favourite java IDE e.g eclipse, intellij, NetBeans.
+ Make sure you have javaFx setup in your IDE.
+ You may need to include the libraries in the lib folder into your class path.
+ Open the main package and run Main.java class *enjoy !*.

### Important Information

<details>
  <summary> <b> Dependencies </b></summary>
  <p>
    1) JDK 1.8 or later. <br>
    2) javaFx library.    <br>
    3) Internet Connection.
  </p>
</details>

