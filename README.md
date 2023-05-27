# read_me_file

ES6: Use the Rest Parameter with Function Parameters
const sum = (...args) => {
  return args.reduce((a, b) => a + b, 0);
}
  
 //============================================================== 
  
ES6: Use Destructuring Assignment to Extract Values from Objects
const HIGH_TEMPERATURES = {
  yesterday: 75,
  today: 77,
  tomorrow: 80
};

// Only change code below this line
  
const [highToday,highTomorrow] = HIGH_TEMPERATURES;

 
 //============================================================== 


ES6: Use Destructuring Assignment to Assign Variables from Objects
const HIGH_TEMPERATURES = {
  yesterday: 75,
  today: 77,
  tomorrow: 80
};

// Only change code below this line
  
const {today: highToday, tomorrow: highTomorrow} = HIGH_TEMPERATURES;

 
 //============================================================== 

ES6: Use Destructuring Assignment to Assign Variables from Nested Objects
const LOCAL_FORECAST = {
  yesterday: { low: 61, high: 75 },
  today: { low: 64, high: 77 },
  tomorrow: { low: 68, high: 80 }
};

// Only change code below this line
  
const {today: {low: lowToday, high: highToday}} = LOCAL_FORECAST;

 
 //============================================================== 

ES6: Use Destructuring Assignment to Assign Variables from Arrays
let a = 8, b = 6;
// Only change code below this line
[a,b] = [b,a];

 
 //============================================================== 

ES6: Use Destructuring Assignment with the Rest Parameter to Reassign Array Elements
const source = [1,2,3,4,5,6,7,8,9,10];
function removeFirstTwo(list) {
  // Only change code below this line
  const [a,b,...arr] = list; // Change this line
  // Only change code above this line
  return arr;
}
const arr = removeFirstTwo(source);

 
 //============================================================== 

ES6: Use Destructuring Assignment to Pass an Object as a Function's Parameters
const stats = {
  max: 56.78,
  standard_deviation: 4.34,
  median: 34.54,
  mode: 23.87,
  min: -0.75,
  average: 35.85
};

// Only change code below this line
const half = ({min, max}) => (max + min) / 2.0; 
// Only change code above this line

 
 //============================================================== 

ES6: Create Strings using Template Literals
const result = {
  success: ["max-length", "no-amd", "prefer-arrow-functions"],
  failure: ["no-var", "var-on-top", "linebreak"],
  skipped: ["no-extra-semi", "no-dup-keys"]
};
function makeList(arr) {
  // Only change code below this line
  const failureItems = [];
  // Only change code above this line
  for (let i = 0; i < arr.length; i++){
    failureItems.push(`<li class="text-warning">${arr[i]}</li>`);
  }

  return failureItems;
}

const failuresList = makeList(result.failure);

 
 //============================================================== 

ES6: Write Concise Object Literal Declarations Using Object Property Shorthand
const createPerson = (name, age, gender) => ({name,age,gender});

 
 //============================================================== 

ES6: Write Concise Declarative Functions with ES6
// Only change code below this line
const bicycle = {
  gear: 2,
  setGear(newGear) {
    this.gear = newGear;
  }
};
// Only change code above this line
bicycle.setGear(3);
console.log(bicycle.gear);

 
 //============================================================== 

ES6: Use class Syntax to Define a Constructor Function
// Only change code below this line
class Vegetable{
    constructor(name){
        this.name = name;
    }
}
// Only change code above this line

const carrot = new Vegetable('carrot');
console.log(carrot.name); // Should display 'carrot'

 
 //============================================================== 

ES6: Use getters and setters to Control Access to an Object
// Only change code below this line
class Thermostat{
    constructor(fahrenheit){
        this.fahrenheit = fahrenheit;
    }

    get temperature(){
        return (5 / 9) * (this.fahrenheit - 32);
    }

    set temperature(celsius){
        this.fahrenheit = (celsius * 9.0) / 5 + 32;
    }
}
// Only change code above this line

const thermos = new Thermostat(76); // Setting in Fahrenheit scale
let temp = thermos.temperature; // 24.44 in Celsius
thermos.temperature = 26;
temp = thermos.temperature; // 26 in Celsius

 
 //============================================================== 

ES6: Create a Module Script
<html>
  <body>
    <!-- Only change code below this line -->
    <script type="module" src="index.js"></script>
    <!-- Only change code above this line -->
  </body>
</html>

 
 //============================================================== 

ES6: Use export to Share a Code Block
const uppercaseString = (string) => {
  return string.toUpperCase();
}

const lowercaseString = (string) => {
  return string.toLowerCase()
}

export {uppercaseString, lowercaseString};

 
 //============================================================== 

ES6: Reuse JavaScript Code Using import
import {uppercaseString, lowercaseString} from './string_functions.js';  
// Only change code above this line

uppercaseString("hello");
lowercaseString("WORLD!");

 
 //============================================================== 

ES6: Use * to Import Everything from a File
// Only change code above this line
import * as stringFunctions from "./string_functions.js";
stringFunctions.uppercaseString("hello");
stringFunctions.lowercaseString("WORLD!");

 
 //============================================================== 

ES6: Create an Export Fallback with export default
export default function subtract(x, y) {
  return x - y;
}

 
 //============================================================== 

ES6: Import a Default Export
import subtract from "./math_functions.js";
// Only change code above this line

subtract(7,4);

 
 //============================================================== 

ES6: Create a JavaScript Promise (usually asynchronously)
const makeServerRequest = new Promise((resolve, reject) => {

});

 
 //============================================================== 

ES6: Complete a Promise with resolve and reject
const makeServerRequest = new Promise((resolve, reject) => {
  // responseFromServer represents a response from a server
  let responseFromServer;
    
  if(responseFromServer) {
    // Change this line
    resolve("We got the data");
  } else {  
    // Change this line
    reject("Data not received");
  }
});

 
 //============================================================== 

ES6: Handle a Fulfilled Promise with then
const makeServerRequest = new Promise((resolve, reject) => {
  // responseFromServer is set to true to represent a successful response from a server
  let responseFromServer = true;
    
  if(responseFromServer) {
    resolve("We got the data");
  } else {  
    reject("Data not received");
  }
});

makeServerRequest.then(result => {
  console.log(result);
});

 
 //============================================================== 

ES6: Handle a Rejected Promise with catch
const makeServerRequest = new Promise((resolve, reject) => {
  // responseFromServer is set to false to represent an unsuccessful response from a server
  let responseFromServer = false;
    
  if(responseFromServer) {
    resolve("We got the data");
  } else {  
    reject("Data not received");
  }
});

makeServerRequest.then(result => {
  console.log(result);
});

makeServerRequest.catch(error => {
  console.log(error);
});
