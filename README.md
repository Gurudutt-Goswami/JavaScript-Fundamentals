# JavaScript Fundamentals
First of all, inspect element in any website & then go to console (short cut open console is Ctrl+ Shift+ i) & perform any calculation. You can also use this to print anything using console.log (“Hello World”) or alert (“Hello World”). It doesn’t need internet to run.


### JavaScript: Client Side Scripting (High Level Dynamic Interpreted Language) 

1)	In case you want to run JS outside the web browser then you can use node.js.
2)	It can be executed on browser as well as server.
3)	There are languages the get trans piled into JS like Coffee Script, TypeScript etc
4)	OOP’s concept can also be easy to implement.
5)	It can be used for both front & backend (node & mongoDB)

### How to Include Js in HTML
````
<script src="FileName.js"></script>
````
## Topics 
1) [JS Console API](#JavaScript-Console-API)
2) [Data Types & Declaring Variables](#Data-Type-&-Declaring-Variables)&nbsp; ([Numbers](#Numbers),[String](#String),[Undefined](#Undefined),[Boolean](#Boolean),[Null](#null),[Arrays](#Arrays),[Objects](#Objects) )
3) [Operators](#Operators)&nbsp; ([Arithmetic](#Arithmetics), [Comparoson](#Comaparison), [Logical](#Logical)  )
4) [Conditionals](#Conditionals)
5) [Loops](#Loops)
6) [Break & continue](#Break-,-continue)
7) [Array Functions](#Array-Functions)
8) [String Functions](#String-Functions)
9) [Date Functions](#Date-Functions)
10) [DOM Manipulation Methods](#DOM-Manipulation-Methods)
11) [Fetch Instant Elements on any sites](#Fetch-Instant-Elements-on-any-sites)
12) [Functions](#Functions)
13) [Event Listeners](#Event-Listeners)
14) [SetTimeOut / SetInterval](#SetTimeout-&-SetInterval)
15) [Local Storage](#Local-Storage)
16) [JSON](#JSON)
17) [Other Basic Things](#Other-Basic-Things)

### JavaScript Console API
````
console.log("Hello World!",4+6,”Fine !”)    //If you want to print anything on console
console.warn("this is a warning !")         //To print warning in console
console.error("this is an error")           //To print error in console
console.assert(4==6)                        //To check for any assertion, will give error on wrong condition
console.clear()                             //To clear the console
````

### Data Type & Declaring Variables
1) Primitive: Data Types that are not made up of anything like undefined, null, number, string, Boolean, symbol
2) Reference Data Type: Arrays & Objects 

#### Numbers
````
var num1 = 123
var num2 = 345.5
console.log(num1+num2)
````
#### String
````
Str1 = “Gurudutt”
Str2 = “Goswami”
Console.log(Str1+Str2)
````

#### Undefined
````
var und = undefined
var und1;
console.log(und, und1)
/*In case you don’t specify any value for a variable & print it even then its
value is going to be undefined */
````
#### Boolean
````
a = true
b = false
console.log(a, b)
````

#### Null
````
n = null
console.log(n)
````

#### Arrays
````
var arr = [1,3,2,5, true, "Fight Club",45.6,88,23]
console.log(arr)
````
#### Objects
````
var marks = {
Ravi : 56,
Sanjeev : 78,
Ashish: 84,
Deepak : 67
}
Console.log(marks)
````

### Operators

#### Arithmetic Operators 
````
var a = 100
var b = 50
console.log("The value of a+b is ",a+b)
console.log("The value of a-b is ",a-b)
console.log("The value of a*b is ",a*b)
console.log("The value of a/b is ",a/b)
console.log("The value of a%b is ",a%b)
````

#### Comparison Operators
````
console.log("The value of a>b is ",a>b)
console.log("The value of a>=b is ",a>=b)
console.log("The value of a<b is ",a<b)
console.log("The value of a<=b is ",a<=b)
console.log("The value of a==b is ",a==b)
````

#### Logical Operators 
#### AND ( && )
````
console.log(true && true)
console.log(true && false)
console.log(false && false)
````
#### OR ( || )
````
console.log(true || true)
console.log(true || false)
console.log(false || false)
````
#### Note: Single vertical line is bitwise operator

#### NOT ( ! )
````
console.log(!true)
console.log(!false)
````
### Conditionals
````
if(a>b)
{console.log("A is greater than B")}
else
{console.log("B is greater than A")}
````
#### Note: Any type of conditionals is possible like only if statement, multiple if statements, if else statements & if, else if, else (ladder if else statements) 


### Loops
````
names = ["Anurag","Deepak","Shudhanshu","Prasoon","Abhishek",”Prabhat"]
console.log(names)

//For loop
for(i=0;i<names.length;i++)
{console.log(names[i])}

//foreach loop
names.forEach(function(element)
{console.log(element);})

//while loop
var j=0
while(j<names.length)
{console.log(names[j])
j++;}

//do while loop
do{
console.log(names[j])
j++;
}while(j<names.length)
````


### Break , continue
````
Num_array = [12,3,4,5,56,74,7,6,8,7,464,46,3]
for(i=0;i<Num_array.length;i++)
{   
    if(i==3)
    {
        //break;
        continue;
    }
    console.log(Num_array[i])
}
````
### Array Functions
````
new_array = [12,3,4,5,56,74,7,6,8,7,464,46,3,23,4,2,5,3,5,2,35,3,35,5,3]
new_array.length
new_array.pop()
new_array.push("Gurudutt")
new_array.shift()
new_array.unshift("Horse");
console.log(new_array.toString())
console.log(new_array.sort())
console.log(new_array);
````
#### For more on Array functions visit: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array

### String Functions
````
var good_str = "Gurudutt Goswami is a good programmer good"
good_str.length
console.log(good_str.indexOf("good"))
console.log(good_str.lastIndexOf("good"))
console.log(good_str.slice(9,16))
d = good_str.replace("programmer","Artist")
console.log(d,good_str)
````
#### For more on String Functions visit : https://www.w3schools.com/js/js_string_methods.asp

### Date/Date Functions
````
var date = new Date()
console.log(date)
console.log(date.getDay())
console.log(date.getHours())
console.log(date.getMilliseconds())
console.log(date.getMonth())
console.log(date.getSeconds())
````

### DOM Manipulation Methods
````
var l = document.getElementById("click")
console.log(l)

var l1 = document.getElementsByClassName("container")
console.log(l1);
// l1[0].style.background = "yellow"
l1[0].classList.add("bg-primary")
l1[0].classList.add("text-success")
l1[0].classList.remove("text-success")
console.log(l1[0].innerHTML)
console.log(l1[0].innerText)

var l2= document.getElementsByTagName("div")
console.log(l2)

//Note 0 means l2 first div if I write 1 then it means l2 second div
createdElement = document.createElement('p');
createdElement.innerText = "This is a new paragraph by using JavaScript Only"
l2[0].appendChild(createdElement)

createdElement2 = document.createElement('b');
createdElement2.innerText = "This is a new paragraph by using JavaScript Only bold statement"
l2[0].replaceChild(createdElement2, createdElement)
````


### Fetch Instant Elements on any sites
````
console.log(document.location)
console.log(document.title)
console.log(document.URL)
console.log(document.scripts)
console.log(document.forms)
console.log(document.links)
console.log(document.domain)
console.log(document.images)

sel = document.querySelector('.container')
console.log(sel)

sel1 = document.querySelectorAll('.container')
console.log(sel1)
````

### Function Syntax
````
function sum(a,b)
{ console.log(a+b)
return a+b}
sum(4,5)

//Arrow Function 
summ = (a,b) => {
console.log(a+b)
return a+b}
summ(56,34)
````

### Event Listeners
````
function Clicked()
{console.log("The button was clicked !")}

window.onload = function()
{ console.log("The document was loaded successfully !")}



firstContainer.addEventListener('click',function()
{
    document.querySelectorAll('.container')[1].innerHTML = "<b> We have cliked this container "
    console.log("Clicked on Container !")
})

firstContainer.addEventListener('mouseover',function()
{console.log("mouse over on Container !")
})

previous_html = document.querySelectorAll('.container')[1].innerHTML
firstContainer.addEventListener('mouseup',function()
{
    document.querySelectorAll('.container')[1].innerHTML = previous_html
    console.log("mouse up on Container !")
})

firstContainer.addEventListener('mousedown',function()
{
    document.querySelectorAll('.container')[1].innerHTML = "<b> We have cliked this container "
    console.log("mouse down on Container !")
})
````


### SetTimeout & SetInterval
````
funny = () => {
    document.querySelectorAll('.container')[1].innerHTML = "Set Time out Invoked "
    console.log("Triggering SetTimeOut")
}
//SetTimeOut is used when you want to invoke a function after certain time 
//To stop its execution one can write clearTimeout(clr) in console
clr = setTimeout(funny,2000) 

//Set Interval is going to run continuosly after each 2 sec 
//To stop its execution you can write clearInterval(clr1) in console
clr1 = setInterval(funny,2000)
````

### Local Storage
Try not to store secure information on localstorages as it can be seen from Application tab from inspect element 
````
console.log(localStorage.setItem('Age','28'))
console.log(localStorage.getItem('Name'))
console.log(localStorage.removeItem('Name'))
localStorage.clear()
console.log(localStorage)
````
### JSON
````
//The JSON standard requires double quotes and will not accept single quotes, nor will the parser.
obj1 = {name : "Guru",length: 97,a:{fun:"this is funny"}}
str_equi = JSON.stringify(obj1)
console.log(typeof str_equi)
console.log(str_equi)
json_equi = JSON.parse(`{"name":"Guru","length":97,"a":{"fun":"this is funny"}}`)
console.log(json_equi)
````

### Other Basic Things 
#### Template Literals
````
a1 = 546
console.log(`The value of a is ${a1}`)
````
#### This is to perform click in console using any class
````
Document.querySelector(“.something”).click()
````

#### You can also search an element by class or id in console using 
````
document.getElementById(id)
````
#### Alert
````
alert("This is an Alert!") #If you want to display anything in MessageBox
````

#### Shorthands
````
a +=10	// a = a+10
a -=10
a *=10
a /=10
console.log(a)
````

