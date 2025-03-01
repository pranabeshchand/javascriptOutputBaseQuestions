# javascript Output Base Questions and Answers

Explore the world of JavaScript through practical output-based questions

---

**1. What will be the output**
```js
let arr = [3, 4, 3, 2, 3, 4, 5, -6, 7];
arr.length = 0;
console.log(arr);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : [ ]</li>
	<li><b>Reason</b> : The length of the array has been set to 0, so the array becomes empty.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**2. What will be the output**
```js
x = 10;
console.log(x);
var x;
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 10</li>
	<li><b>Reason</b> : The declaration of the variable x is hoisted to the top of its scope.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**3. What will be the output**
```js
let a = { x: 1, y: 2 }
let b = a;
b.x = 3;
console.log(a);
console.log(b);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : { x: 3, y: 2 } { x: 3, y: 2 }</li>
	<li><b>Reason</b> : 'a' and 'b' both are pointing to the same reference.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**4. What will be the output**
```js
for(var i = 0; i < 10; i++){
    setTimeout(function(){
      console.log("value is " + i);
  })
}
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 10 times, "value is 10"</li>
	<li><b>Reason</b> : "var" has a function scope, and there will be only one shared binding for the iterations. By the time the setTimeout function gets executed, the for loop has already completed and the value of the variable i is 10.</li>
</ul>
</details> 

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**5. What will be the output**
```js
for(let i = 0; i < 10; i++){
    setTimeout(function(){
      console.log("value is " + i);
  })
}
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 10 times "value is" followed by the value of i in each iteration, from 0 to 9</li>
	<li><b>Reason</b> : "let" has a block scope, and a new binding will be created for each iteration. Here, a new variable i is created and has a different value for each iteration of the loop.</li>
</ul>
</details> 

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**6. What will be the output**
```js
function hello() {
  console.log("1");
    setTimeout(() => {
        console.log("2");
    })
  console.log("3");
}
hello();
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : "1" followed by "3", and then after a small delay, "2"</li>
	<li><b>Reason</b> : console.log("1") statement logs "1" to the console. Then setTimeout() function is set to execute the callback function in the next event loop iteration and logs "3" to the console.</li>
</ul>
</details> 

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**7. What will be the output**
```js
let f = "8";
let a = 1;
console.log((+f)+a+1);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 10</li>
	<li><b>Reason</b> : The expression (+f) is a shorthand way to convert the string value of f to a number. Therefore, (+f) evaluates to 8.</li>
</ul>
</details> 

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**8. What will be the output**
```js
let a = 10;
if(true){
   let a = 20;
   console.log(a, "inside");
}
console.log(a, "outside");
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 20, "inside" and 10, "outside"</li>
	<li><b>Reason</b> : The variable "a" declared inside "if" has block scope and does not affect the value of the outer "a" variable.</li>
</ul>
</details> 

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**9. What will be the output**
```js
var a = "xyz";
var a = "pqr";
console.log(a)
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : "pqr"</li>
	<li><b>Reason</b> : Both the variables are declared using "var" keyword with the same name "a". The second variable declaration will override the first variable declaration.</li>
</ul>
</details> 

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**10. What will be the output**
```js
const arr1 = [1, 2, 3, 4];
const arr2 = [6, 7, 5];
const result = [...arr1, ...arr2];
console.log(result);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : [1, 2, 3, 4, 6, 7, 5]</li>
	<li><b>Reason</b> : Spread operator (...) concatenates the two arrays into "result" array.</li>
</ul>
</details> 

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**11. What will be the output**
```js
const person1 = { name: 'xyz', age: 21 };
const person2 = { city: 'abc', ...person1 };
console.log(person2);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : { city: 'abc', name: 'xyz', age: 21 }</li>
	<li><b>Reason</b> : Spread operator (...) copies all the properties from person1 into person2.</li>
</ul>
</details> 

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**12. What will be the output**
```js
console.log(5 < 6 < 7);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : true</li>
	<li><b>Reason</b> : In JavaScript, the < operator evaluates expressions from left to right. First, the expression 5 < 6 is evaluated, resulting in true because 5 is less than 6. Then, the expression true < 7 is evaluated. In this case, JavaScript performs type coercion and converts true to the number 1. Therefore, the expression becomes 1 < 7, which is true.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**13. What will be the output**
```js
console.log(7 > 6 > 5);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : false</li>
	<li><b>Reason</b> : In JavaScript, the > operator evaluates expressions from left to right. First, the expression 7 > 6 is evaluated, resulting in true because 7 is greater than 6. Then, the expression true > 5 is evaluated. In this case, JavaScript performs type coercion and converts true to the number 1. Therefore, the expression becomes 1 > 5, which is false.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**14. What will be the output**
```js
console.log(0 == false);
console.log(1 == true);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : true, true</li>
	<li><b>Reason</b> : The == operator converts operands to a common type before making the comparison. In both the cases, the boolean value will be converted to a number, i.e., false is converted to 0 and true is converted to 1. So, the expression 0 == false is equivalent to 0 == 0 and 1 == true is equivalent to 1 == 1.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**15. What will be the output**
```js
console.log([11, 2, 31] + [4, 5, 6]);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : "11,2,314,5,6"</li>
	<li><b>Reason</b> : The + operator is used for both addition and string concatenation. When you try to concatenate two arrays using the + operator, the arrays are converted to strings and then concatenated together. In this case, the arrays [11, 2, 31] and [4, 5, 6] are converted to strings as "11,2,31" and "4,5,6" respectively. Then, the two strings are concatenated, resulting in "11,2,314,5,6".</li>
</ul>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**16. What will be the output**
```js
console.log({} == {}); 
console.log({} === {});
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : false, false</li>
	<li><b>Reason</b> : When you compare objects using == or ===, it checks if they refer to the exact same object. So even if they are looking same, they are pointing to different memory locations.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**17. What will be the output**
```js
let x = 5;
let y = x++;
console.log(y);
console.log(x)
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 5, 6</li>
	<li><b>Reason</b> : The post-increment operator increments and returns the value before incrementing.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**18. What will be the output**
```js
let x = 5;
let y = ++x;
console.log(y);
console.log(x)
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 6, 6</li>
	<li><b>Reason</b> : The pre-increment operator increments and returns the value after incrementing.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**19. What will be the output**
```js
console.log('apple'.split(''));
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : [ 'a', 'p', 'p', 'l', 'e' ]</li>
	<li><b>Reason</b> : split method is used to split a string into an array of substrings based on a specified separator. </li>
</ul>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**20. What will be the output**
```js
const arr = [2,3,5,2,8,10,5];
console.log(arr.indexOf(5))
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 2</li>
	<li><b>Reason</b> : indexOf method returns the index of the first occurrence of the specified element in the array. </li>
</ul>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**21. What will be the output**
```js
const array = [8, 18, 28, 38];
const result = array.map(element => element + 2)
               .filter((element) => element > 25);
console.log(result);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : [ 30, 40 ]</li>
	<li><b>Reason</b> : The code increments each element in the array by 2 using map and filters out elements greater than 25 using filter.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**22. What will be the output**
```js
function checkValue(value){
    var result = Array.isArray(value);
    console.log(result);
}
checkValue([1,2,3]);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : true</li>
	<li><b>Reason</b> : Array.isArray() method is used to check if the provided value is an array.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**23. What will be the output**
```js
function sum(a=5, b=7){
    return a+b;
}
console.log(sum(undefined, 20));
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 25</li>
	<li><b>Reason</b> : Here, undefined is passed as the value for parameter a, and 20 is passed for parameter b. When any parameter is undefined, the default value is used. </li>
</ul>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**24. What will be the output**
```js
console.log(10 + "5");
console.log("5" + 10);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 105, 510</li>
	<li><b>Reason</b> : Since one operand is a string, the + operator performs string concatenation. </li>
</ul>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**25. What will be the output**
```js
console.log(10 - "5");
console.log("5" - 10);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 5, -5</li>
	<li><b>Reason</b> : In JavaScript, when the subtraction operator - is used, the operands are converted to numbers before performing the subtraction </li>
</ul>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**26. What will be the output**
```js
console.log(printName());
function printName(){
    return "Hi my name is Bob"
}
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : Hi my name is Bob</li>
	<li><b>Reason</b> : Regular functions are hoisted to the top. And you can access and call them even before they are declared. </li>
</ul>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**


**27. What will be the output**
```js
console.log(printName());
const printName = () => {
    return "Hi my name is Bob"
}
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : ReferenceError: Cannot access 'printName' before initialization</li>
	<li><b>Reason</b> : Arrow functions cannot be accessed before they are initialised. </li>
</ul>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**28. What will be the output (shallow copy of an object)**
```js
const userDetails = {
  firstName: "Surbhi",
  lastName: "Dighe",
  age: 20,
  address: {
    city: "Hyderabad",
    country: "India",
  },
};

let cloneUserDetails = { ...userDetails };
//Updating original object
userDetails.age = 22;
userDetails.address.city = "Banglore";

console.log(cloneUserDetails.age); 
console.log(cloneUserDetails.address.city);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 20, "Banglore"</li>
	<li><b>Reason </b> : cloneUserDetails is created by using the spread syntax ({ ...userDetails }). This syntax creates a shallow copy of the userDetails object, meaning that the top-level properties are copied, but nested objects are still referenced.</li>
	<li><b>case 1</b> : Although userDetails.age was changed to 22, cloneUserDetails still holds the original value of 20. This is because the spread syntax only creates a shallow copy, so the age property of cloneUserDetails remains unchanged.</li>
	<li><b>case 2</b> : The nested address object is still referenced by cloneUserDetails, so when the city property of userDetails.address is changed, it reflects in cloneUserDetails.address as well. Therefore, the output is "Banglore".</li>
	</ul>

</ul>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**29. What will be the output**
```js
function hello(){
console.log(name);
console.log(age);
var name = "Alice";
let age = 21;
}
hello();
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : undefined, ReferenceError: can't access lexical declaration 'age' before initialization"</li>
	<li><b>Reason for console.log(name)</b> : The variable name (declared with var) is hoisted to the top, so JavaScript knows it exists, but it hasn't been assigned a value yet, so it prints undefined</li>
	<li><b>Reason for console.log(age)</b> : The variable age (declared with let) is also hoisted to the top of its scope, but unlike var, it is not initialized until the line where it is declared.</b></li>
</ul>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**


**30. What will be the output**
```js
const arr1 = [1,2,3];
const arr2 = [1,2,3];
const str = "1,2,3";

console.log(arr1 == str);
console.log(arr1 == arr2);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : true, false</li>
	<li><b>Reason for console.log(arr1 == str)</b> : Javascript compiler performs type conversion. In this case, it converts the array arr1 and the string str to their string representations and then compares them.</li>
	<li><b>Reason for console.log(arr1==arr2) </b> : In Javascript arrays are objects and objects are compared by reference. In this case, arr1 and arr2 are pointing to 2 different memory locations</b></li>
</ul>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**31. What will be the output**
```js
const a = {x : 1};
const b = {x : 1};
console.log(a === b);
console.log(a.x === b.x)
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : false, true</li>
	<li><b>Reason for console.log(a === b)</b> : This compares whether a and b refer to the exact same object in memory. They are two different objects in memory, so the comparison evaluates to false</li>
	<li><b>Reason for console.log(a.x === b.x)</b> : This compares the x property of objects a and b. Since both a.x and b.x have the same value i.e., 1, so the comparison evaluates to true.</b></li>
</ul>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**32. What will be the output**
```js
const arr = [10, -1, 2];
arr.sort((a, b) => a - b);
console.log(arr);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : [-1, 2, 10]</li>
	<li><b>Reason</b> : The compare function (a, b) => a - b sorts the numbers numerically in ascending order.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**33. What will be the output**
```js
const arr = [11, 0, '', false, 2, 1];
const filtered = arr.filter(Boolean);
console.log(filtered);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : [11, 2, 1]</li>
	<li><b>Reason</b> : filter(Boolean) removes all falsy values (0, "" (empty string), false, null, undefined, and NaN) from the array and keeps truthy ones.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**34. What will be the output**
```js
var x = 0;
var y = 10;
if(x){
  console.log(x);
}
if(y){
  console.log(y);
}
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 10</li>
	<li><b>Reason</b> : x = 0 is falsy and doesn't trigger the console.log(x), while y = 10 is truthy and triggers the console.log(y).</li>
</ul>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**35. What will be the output**
```js
const obj = {
var1: 1,
var2: 2
};
const { var1, var2 } = obj;
console.log(var1, var2);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 1, 2</li>
	<li><b>Reason</b> : Object destructuring extracts the values of var1 and var2 from obj object and prints them using console.log(var1, var2)</li>
</ul>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**36. What will be the output**
```js
const user = { 
name: "Surbhi dighe", 
country: "India" 
};
const { name: fullname, country } = user;
console.log(fullname);
console.log(name);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : Surbhi Dighe, ReferenceError: name is not defined</li>
	<li><b>Reason for console.log(fullname)</b> : The name property from user is assigned to a local variable fullname.</li>
	<li><b>Reason for console.log(name)</b> : It gives an error because name was assigned to a local variable fullname and therefore name is not directly accessible.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**37. What will be the output**
```js
const person = {
  firstName: 'Surbhi',
};
const { lastName="dighe" } = person;
console.log(lastName);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : dighe</li>
	<li><b>Reason</b> : The lastName property is not defined in the person object and the destructuring syntax provides a default value ("dighe") to be used when the property is missing.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**38. What will be the output**
```js
const person = {
  firstName: 'Surbhi',
};
const { firstName="Henry"} = person;
console.log(firstName);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : Surbhi</li>
	<li><b>Reason</b> : The `firstName` property in the `person` object has the value 'Surbhi'. The default value "Henry" is ignored because it only applies when the property does not exist or is `undefined`</li>
</ul>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**39. What will be the output**
```js
var a = 10;
let a = 20;
console.log(a)
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : SyntaxError: Identifier 'a' has already been declared</li>
	<li><b>Reason</b> : In Javascript, we cannot redeclare a variable with let if it has already been declared in the same scope. </li>
</ul>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**40. What will be the output**
```js
const arr = ["A","B","C","D","E"]
console.log(Object.keys(arr)); 
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : [ '0', '1', '2', '3', '4' ]</li>
	<li><b>Reason</b> : In JavaScript, arrays are a special type of object. Object.keys() on an array returns an array of strings representing the indices of the array elements. </li>
</ul>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**41. Consider the two functions below. Will they both return the same thing?**
```js
function foo1()
{
return {
bar: "hello"
};
}
function foo2()
{
return
{
bar: "hello"
};
} 
```
<details>
	<summary><b>View Answer</b></summary>
<p>Surprisingly, no. JavaScript is very fogiving of missed semi-colons, so when you write a statement in new line without ending it with a <code>;</code>, it is automatically inserted by the engine. That will result in <code>foo2</code> returning <code>undefined</code>, while <code>foo1</code> an <code>object</code>.</p>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**42. What will be the output of the following code?**
```js
var z = 1, y = z = typeof y;
console.log(y);
```
<details>
	<summary><b>View Answer</b></summary>
<p>The above code will output <code>undefined</code>. The order of execution with the <code>=</code> operator is right to left, which means <code>typeof y</code> will execute first and will return <code>undefined</code>, which will then pass to <code>z</code> and <code>y</code>. Thus, <code>console.log(y);</code> will print <code>undefined</code>.</p>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**43. What will be the output of the following code?**
```js
var Employee = {
company: 'Acme'
}
var employee1 = Object.create(Employee);
delete employee1.company
console.log(employee1.company);
```
<details>
	<summary><b>View Answer</b></summary>
<p>The above code will output <code>Acme</code>. For the object <code>employee1</code>, <code>company</code> is a prototype property that can't be deleted using the <code>delete</code> operator.</p>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**44. What will be the output**
```js
var a = [1, 2, 3];
a[10] = 99;
console.log(a[6]);
```
<details>
	<summary><b>View Answer</b></summary>
<p>When doing <code>a[10] = 99;</code> the JavaScript engine will set the array slots from 3 to 9 to an empty value. That would equal a declared, but not defined variable. Accordingly, doing <code>console.log(a[6]);</code> will print <code>undefined</code>.</p>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**45. What is JavaScript self-invoking anonymous function?**
```js 
```
<details>
	<summary><b>View Answer</b></summary>
<p><p>A self-invoking anonymous function runs immediately when we define it and doesn't have a name. E.g. </p><pre><code class="javascript">(function() {<div style="text-indent: 10px">console.log("this will print automatically");</div>})();</code></pre></p>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**46. What is the difference between a method and a function in javascript?**
```js 
```
<details>
	<summary><b>View Answer</b></summary>
<p><p>A function is a piece of code that is called by name and it is not associated with any object, nor defined inside an object. It can be passed data to operate on (i.e. parameter) and can optionally return data (the return value). E.g.:</p><pre><code class="javascript">/* Function definition*/<br>function myFunc() {<div style="text-indent: 10px">/* Do some stuff; */</div>}<br>myFunc();/* Calling the function */</code></pre><p>A method is a piece of code that is called by name and is defined inside an object. It is almost identical to a function except that it is always associated with an object and operating only on data inside it.</p><pre><code class="javascript">var methodObject = {<div style="text-indent: 10px">attribute: "xyz",</div><div style="text-indent: 10px">display: function () {  /* Method*/</div><div style="text-indent: 20px">console.log(this.attribute);</div><div style="text-indent: 10px">}</div>}methodObject.display(); /* Calling the method */</code></pre></p>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**47. Why would you use use strict at the beginning of a JavaScript source file?**
```js 
```
<details>
	<summary><b>View Answer</b></summary>
<p><p>Using strict is a way to enforce strict parsing and error handling of the JavaScript code at runtime. This means that code errors that would have otherwise been ignored or would have failed silently, will now generate errors or throw exceptions.</p><p>Some benefits are: easier debugging; preventing accidental globals, eliminates misuse of <code>this</code> etc.</p></p>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**

**48. What is the reason for wrapping the entire content of a JavaScript source file in a function block?**
```js 
```
<details>
	<summary><b>View Answer</b></summary>
<p>This is a common practice used in many popular JavaScript libraries (jQuery, Node.js, etc.). It creates a closure around the entire contents of the file which makes a private namespace and thereby avoids potential name clashes between different JavaScript modules and libraries.</p>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**
**49. What is prototype property in JavaScript?**
```js
let arr = [3, 4, 3, 2, 3, 4, 5, -6, 7];
arr.length = 0;
console.log(arr);
```
<details>
	<summary><b>View Answer</b></summary>
<p>Every JavaScript function has a prototype property (by default this property is null), that is mainly used for implementing inheritance. We add methods and properties to a function's prototype so that it becomes available to instances of that function.</p>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**
**50. Explain the difference between class inheritance and prototypal inheritance.**
```js 
```
<details>
	<summary><b>View Answer</b></summary>
<p><p></p><ul><li>Class Inheritance: A constructor function instantiates an instance via the "new" keyword. This new instance inherits properties from a parent class.</li><li>Prototypal Inheritance: An instance is created by cloning an existing object that serves as a prototype. Instances are typically instantiated via factory functions, object literals, or <code>Object.create()</code>. Instances may be composed from many different source objects, allowing for easy selective inheritance.</li></ul><p></p></p>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**
**51. How to call other class methods?**
```js 
```
<details>
	<summary><b>View Answer</b></summary>
<p><p>Using <code>call()</code> and <code>apply()</code> method we can use methods from different context to the current context. It is really helpful for code reusability and context binding.</p><ul><li><code>call()</code>: is used to call a function with a given <code>this</code> value and arguments provided individually.</li><li><code>apply()</code>: is used to call a function with a given <code>this</code> value and arguments provided as an array.</li></ul></p>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**
**52. What is Scope in JavaScript?**
```js 
```
<details>
	<summary><b>View Answer</b></summary>
<p><p>The scope determines the accessibility of variables, objects, and functions in particular part of your code.</p><p>In JavaScript, the scope can be of two types.</p><ul><li>1. Global Scope</li><li>2. Local Scope</li></ul></p>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**
**53. What is the difference between declaring a function in the two formats below?**
```js
var foo = function() {
/* Some code */
};
function bar() {
/* Some code */
};
```
<details>
	<summary><b>View Answer</b></summary>
<p>The main difference is that <code>foo</code> is defined at run-time whereas <code>bar</code> is defined at parse time. E.g.<pre><code class="javascript">/* Run-Time function declaration*/<br>foo(); /* Calling foo here will throw an error */<br>var foo = function() {<div style="text-indent: 10px">console.log("Hi I am inside Foo");</div>};</code></pre><pre><code class="javascript">/* Parse-Time function declaration */<br>bar(); /* Call bar function here, It will not give an Error */<br>function bar() {<div style="text-indent: 10px">console.log("Hi I am inside Foo");</div>};</code></pre></p>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**
**54. How does Array() differ from [] while creating a JavaScript array?**
```js 
```
<details>
	<summary><b>View Answer</b></summary>
<p><p>Both the <code>Array()</code> and <code>[]</code> work almost the same in JavaScript.</p>
                <p>If we use them as is (i.e. without any argument) to create an array object, then they will result in an array object of zero length. Even if we pass a string or a list of strings as arguments, the result will be similar.
                </p><p>However, they differ when the input argument is of integer type. In that case, the <array(n)> statement will create an uninitialized array of size n. Whereas, the <code>[n]</code> statement will create an array of size 1 and assign n as the value of the first element.</array(n)></p></p>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**
**55. What is the result of "10"+20+30 in JavaScript?**
```js 
```
<details>
	<summary><b>View Answer</b></summary>
<p><p>The result is 102030 because when using the <code>+</code> operator with a string, it acts as a string concatenation operator (not binary <code>+</code>). To make it work as expected, you should parse the <code>"10"</code> to integer before doing the <code>+</code>.</p></p>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**
**56. What does the isNaN() function do?**
```js 
```
<details>
	<summary><b>View Answer</b></summary>
<p>The <code>isNan()</code> function returns <code>true</code> if the variable value is not a number.</p>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**
**57. What is the difference between == and ===?**
```js 
```
<details>
	<summary><b>View Answer</b></summary>
<p><p>The <code>==</code> operator checks equality only, whereas <code>===</code> checks equality and data type i.e. the values must be of the same type.</p></p>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**
**58. What will be the output of the code below?**
```js
var trees = ["pine","apple","oak","maple","cherry"];
delete trees[3];
console.log(trees.length);
```
<details>
	<summary><b>View Answer</b></summary>
<p><p>The output would be 5. When we use the <code>delete</code> operator to delete an array element it doesn't unset the element in that position of the array, but sets it to <code>undefined</code> instead. So, the array length is not affected by the <code>delete</code> operation. This holds true even if you deleted all elements of an array using the <code>delete</code> operator.</p></p>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**
**59. What is a "closure" in JavaScript?**
```js 
```
<details>
	<summary><b>View Answer</b></summary>
<p><p>A closure is a function defined inside another function (called the parent function), and has access to variables that are declared and defined in the parent function scope.</p>
                    <p>The closure has access to variables in three scopes:
                        </p><ul>
                            <li>Variables declared in their own scope</li>
                            <li>Variables declared in a parent function scope</li>
                            <li>Variables declared in the global namespace</li>
                        </ul>
                    <p></p></p>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**
**60. What is the difference between undefined and not defined in JavaScript?**
```js 
```
<details>
	<summary><b>View Answer</b></summary>
<p><p>In JavaScript, if you try to use a variable that has not been declared, then JavaScript will throw an error <code>var x is not defined</code> and the script will stop executing. However, if you use <code>typeof undeclared_variable</code>, then it will return <code>undefined</code>.</p><p>Additionally, doing <code>console.log(x)</code>, when x has been declared, but not defined (doesn't have a value yet), will also print <code>undefined</code>.</p></p>
</details>

**[:top: Scroll to Top](#javascriptOutputBaseQuestions)**
