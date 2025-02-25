# JavaScript Coding Snippets For Interview

#### Snippet 1
```javascript
const profile={
    name: 'Kevin',
    getName:()=>{
        console.log('name',this.name);
    }
}
profile.getName();
```

Output:

> name 
#### Snippet 2
```javascript
function Counter() {
	 var count = 0;
	 this.incrementCounter = function() { 
		 count++;
		 console.log(count);
	  } 

	 this.decrementCounter = function() {
		 count--;
		 console.log(count);
	 }
}

var counter1 = new Counter();
counter1.incrementCounter();
counter1.incrementCounter();
counter1.decrementCounter();
```

Output:

> 1
> 2
> 1
#### Snippet 3
```javascript
function x() { 
for(var i = 1; i<=5; i++){ 
	 setTimeout(
	 function() {
		 console.log(i);
		 }, i*1000);
		} 
	 console.log("Welcome to Cogentlabs");
} 

x();
```

Output:

> Welcome to Cogentlabs
> 6
> 6
> 6
> 6
> 6
#### Snippet 4
```javascript
function x() { 
	for(var i = 1; i<=5; i++){
		function close(i){ 
			 setTimeout(
			 function() {
				 console.log(i);
				 }, i*1000);
			} 
		close(i)
	}
	console.log("Welcome to Cogentlabs");
} 

x();
```

Output:

> Welcome to Cogentlabs
> 1
> 2
> 3
> 4
> 5
#### Snippet 5
```javascript
const a = [
	{ name: 'John Wick'},
	{ name: 'Peter Parker'},
]

const b = [...a];

b[1] = { name: 'Batman' };
b[0].age = 23; 

console.log(a);
console.log(b);
```

Output:

> [
	{ age:23, name: 'John Wick'},
	{ name: 'Peter Parker'},
]

>[
	{ age:23, name: 'John Wick'},
	{ name: 'Batman'},
]

#### Snippet 6
```javascript
const obj = a {
	"1": 'a',
	1: 'b',
	[1]: 'c',
}

console.log(obj["1"])
```

Output:

> c

#### Snippet 7
```javascript
const a = [1,2,3];
const b = [...a];
b.push(4)

console.log(a)
```

Output:

> c

#### Snippet 8
```javascript
async function check(){
	await Promise.resolve(console.log(1));
	console.log(2);
}

console.log(3);
check();
console.log(4);

```

Output:

> 3
> 1
> 4
> 2

#### Snippet 9
```javascript
function manipulativeArray(arr){
	arr.push(5);
	arr=[1];
	return arr;
}

let list = [1,2,3,4];
manipulativeArray(list);
console.log(list);

list = manipulativeArray(list);
console.log(list);

```

Output:

> [1, 2, 3, 4, 5]
> [1]

#### Snippet 10
```javascript
function  job() {
	return  new  Promise(function (resolve, reject) {
		reject();
	});
}
let  promise  =  job();
promise
.then(function () {
	console.log('Success 1');
})
.then(function () {
	console.log('Success 2');
})
.then(function () {
	console.log('Success 3');
})
.catch(function () {
	console.log('Error 1');
})
.then(function () {
	console.log('Success 4');
});

```

Output:

> Error 1
> Success 4


#### Snippet 11
```javascript
let name = 'George';
console.log('name => ',name);
function callName(){
	console.log('name => ',name);
	let name='Stuart';
	console.log('name => ',name);
}
callName();
console.log('name => ',name);
```

Output:

> name => George

> Reference ERROR

#### Snippet 12
```javascript
let x = true;
setTimeout(()=>{x=false},1000);
while(x){
	console.log('Welcome User 1');
}
```

Output:

> Welcome User 1 // will be consoled infinitly
