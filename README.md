# this keyword and Arrow function

#### this with normal function
```javascript
var obj = {
	name:'Suryansh',
	getThis: function(){
		console.log(this);
	}
}
obj.getThis(); 
// Parent Object {name: "Suryansh", getThis: ƒ}
```

```javascript
var obj = {
	name:'Suryansh',
	getThis: function(){
		console.log(this);
	}
}
var data = obj.getThis;
data(); 
// Window Object
```

#### this with Arrow function
```javascript
var obj = {
	name:'Suryansh',
	getThis: () => {
		console.log(this);
	}
}
obj.getThis(); // Window Object
```

```javascript
var obj = {
	name:'Suryansh',
	getThis: () => {
		console.log(this);
	}
}
var data = obj.getThis;
data(); 
// Window Object
```

##### Example on this

```javascript
var a = 5;
console.log(a); // 5
console.log(this.a); // 5
console.log(window.a); // 5
```

```javascript
var len = 10;
function foo(){
	var len = 20;
	console.log(this.len);
}
foo();
// 10
```
