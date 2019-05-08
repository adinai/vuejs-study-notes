
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
	// Looping over items in messages array from the data model
	<ul>
	<li v-for ="msg in messages">{{ msg}}</li>
	</ul>
// Looping over the objects in the shoppingItems array.
<ul>
<li v-for="item in shoppingItems">
{{item.name}} - {{item.price}}
</li>
</ul>
```
>> If multiple items should repeat with the v-for directive, we should wrap them in <template> element.
<template v-for="item in shoppingItems">
<label> {{ item.name }}</label>
<label> {{ item.price }}</label>
<button>Buy</button>
</template>
	
In addition to the property value, we get two additional parameters when looping over objects with Vue. Namely, the key and the index values.
<ul>
	<li v-for="(item,key,index) in onjectItems">
		{{ item }} = {{ key }} - {{ index }}
	</li>
	</ul>

v-for with Range
<ul>
	<li v-for="item in 15">{{ item }}</li>
	</ul>

**Managing Changes**
Out of the box v-for supports array mutation methods. These are push, pop, shift, unshift, splice, sort and reverse. 

The two things that Vue can’t track when changed in an array are,
1. Setting items directly
ex: data.shoppingItems[3] = {price: 10, name: 'pineapple'}
This can be resolved by using the Vue.set method. This method accepts the array, an index and the new value.
```javascript
Vue.set(data.shoppingItems, 3,{price:10, name: 'pineapple'});

2. Modifying array length
ex: data.shoppingItems.length = 2


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

 
 




### Course Links
[Course Vue School](https://vueschool.io/courses)
[Vue Mastery](https://www.vuemastery.com/conferences)
[Vue Alligator](https://alligator.io/js/filter-array-method/)
[Hackr.io]( https://hackr.io/tutorial/getting-started-with-vuejs)


