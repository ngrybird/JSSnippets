# JavaScript Snippets
 
 ## var, let & const
 ``` javascript
 1)# 
var a = 30;
(function(){
    console.log(a); //30
    function as(){
        const d = 50;
        let s;
        s = 50;
        console.log(s); //50  
    }    
    as()
    const b = 20;
    console.log(b); //20
})();
```
 ``` javascript
var a = 30;
(function(){
    console.log(a); //30
    function as(){
		console.log(d); //undefined  
        var d = 50;
        let s;
        s = 50;
        console.log(a) // 30
    }    
    as()
    const b = 20;
    console.log(b); //20
})();
 ```

```javascript
2) #
var a = 30;
function some(){
    console.log(a); // 30
}
some()
```

```javascript
3) #
let as1 = 30;
function some(){

    let as1;
    console.log(as1); //undefined
}
some()

```

```javascript
4) #
let a = 30;
function some(){
    console.log(a); // 30
}
some();
```
```javascript
5) #
var c = 30;
function some(){
    var c;
    console.log(c); //undefiend
}
some();
```
```javascript
5) #
function some(){
     var a = 10;
     a;
     console.log(a); //10
}
some()
```

```javascript
var b = 30;
var b = 20; //no Error
console.log(a) // 20
```

```javascript
let b = 30;
let b = 20; //Syntax Error
console.log(a)
```

```javascript
function as(){
	let a = 10
	return function df(){
		let a = 20;
		console.log(a);
	}
}
var outer = as();
outer(); //20
```
```javascript
function as(){
	var a = 10
	return function df(){
		var a = 20;
		console.log(a);
	}
}
var outer = as();
outer(); //20
```

```javascript
typeof('') //"string"
----------------------------
undefined==null //true
----------------------------------
0=='' //true
-----------------------------------------------
typeof("" || null || undefined) //"undefined"
------------------------------------
2+true>(true+false) //true
---------------------------
var test = 500
var result = function(){
	console.log(test);
	var test = 1000;
}
undefined
--------------------------------------------------------
(function(){
	var objA = {
		foo : 'foo',
		bar : 'bar'
	}
	var objB = {
		foo : 'foo',
		bar : 'bar'
	}
	console.log(objA == objB)
	console.log(objA === objB)
}())
VM528:10 false
VM528:11 false
----------------------------
var employeeId = 'aq';
(function(){
	try{
		throw '123'
	}
	catch(employeeId){
		console.log(employeeId)
	}
	console.log(employeeId)
}())
VM879:7 123
VM879:9 aq
--------------------------------------------
(function(){
	var arraNumb = [2,8,15,16,23,42];
	arraNumb.sort();
	console.log(arraNumb)
})();
VM1019:4 (6) [15, 16, 2, 23, 42, 8]
-------------------------------------
for(let i = 1 ;i<=5;i++){
	setTimeout(()=>{console.log(i)},i*1000);
}
12
VM1126:2 1
VM1126:2 2
VM1126:2 3
VM1126:2 4
VM1126:2 5
-------------------------------------------
var arr = [10,32,65,2];
for(var i = 0; i< arr.length ;i++){
	setTimeout(function(j){
		return function(){
			console.log(j)
			}
	}(i),3000)
}
25
VM3342:5 0
VM3342:5 1
VM3342:5 2
VM3342:5 3
----------------------------
[1,2,3,4,5].forEach(i=> {setTimeout(()=>console.log(i),i*1000)})
undefined
VM1243:1 1
VM1243:1 2
VM1243:1 3
VM1243:1 4
VM1243:1 5
---------------------------------
var a = 3
var obj = {
	a : 2,
	foo : {
		a : 1,
		bar : function(){
			return this.a;
		}
	}
}
var test = obj.foo.bar;
alert(test()); //3
alert(obj.foo.bar()); //1
-----------------------------------------------
(function(){
	var array = new Array('100');
	console.log(array);
	console.log(array.length)
}());
VM1876:3 ["100"]
VM1876:4 1
--------------------------------------------------
var person = {name : 'john'};
person.salary = '10000$';
person['country'] = 'SG';
console.log(Object.keys(person))
VM2137:4 (3) ["name", "salary", "country"]
-----------------------------------------------
function Test1(name){
	let a = name;
	function Test2(){
		console.log('output : ',this.a);
	}
	Test2();
}
Test1('dbs') //undefined
--------------------------------------------

var x= 500;
let z,p,q;
q = 200;
x =y=z=p=q;

console.log(q,x,y,z,p)
200 200 200 200 200

-------------------------------------------
function Test1(cname){
	let b = cname;
	test2()
	let c;
	function test2(){
		let c = 'singapur';
		console.log('continent : ',cname);
	}
	console.log('country : ',b,c)
}
Test1('asia')
VM3789:8 continent :  asia
VM3789:10 country :  asia undefined
```
