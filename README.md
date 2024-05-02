# JavaScript-theory-exercises
simple (subjective statement) exercises in JavaScript theory: syntax, object-oriented programming (OOP) etc.
***
***
1. a function that prints the classic "Hello World" in the console, with no arguments passed to it
```
function printHW(){console.log("Hello World!");}
printHW();
```
2. a function that prints the classic "Hello World" in the console, with a string argument passed to the function
```
function printHW(str){console.log(str);}
printHW("Hello World!");
```
3. above function, but written as a value
```
let printHW = function(str){console.log(str);}
printHW("Hello World!");
```
4. nested function
```
function printH(){
  function printW(){return "World";}
  return `Hello ${printW()}!`
}
console.log(printH());
```
5. passing arguments to nested functions
```
function printFinal(word){
  function getLastWord(word){return `Beautiful ${word}`;}
  return `Hello ${getLastWord(word)}!`
}
console.log(printFinal("World"));
```
6. arrow function
```
let sqrOfNum = (num) => {return num * num;}
```
7. a simple class
```
class Animal {
  constructor(weight, dominantColor) {
    this.weight = weight;
    this.dominantColor = dominantColor;
  }
}
let Fido = new Animal(5200, "brown");
console.log(`weight: ${Fido.weight}, color: ${Fido.dominantColor}`);
```