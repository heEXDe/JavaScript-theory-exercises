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
// output: weight: 5200, color: brown
```
8. a class with a method
```
class Animal {
  constructor(weight, dominantColor) {
    this.weight = weight;
    this.dominantColor = dominantColor;
  }
  move(){return "The animal is moving."}
}
let Fido = new Animal(5200, "brown");
console.log(`${Fido.move()}`);
// output: The animal is moving.
```
9. a class with a method using object properties
```
class Animal {
  constructor(weight, dominantColor) {
    this.weight = weight;
    this.dominantColor = dominantColor;
  }
  move(){return "The animal is moving."}
  size(){return this.weight > 2000 ? "it's a medium or large animal" : "it's a small animal"}
}
let Fido = new Animal(5200, "brown");
console.log(`${Fido.size()}`);
// output: it's a medium or large animal
```
10. simple object
```
let obj01 = {
  size: "small",
  dimensions: [12, 3, 7.5],
  // passing an object as a property of object obj01
  paramOfConnecObject: {size: "medium", dimensions: [20, 11, 21], paramOfConnecObject: {}}
}
console.log(`size: ${obj01.size} and dimensions: ${obj01.dimensions} and ${obj01.paramOfConnecObject}`);
```
11. changing properties of an object
```
obj01.dimensions = [12, 3, 10];
console.log(obj01.dimensions);
obj01.dimensions[2] = 7.5;
console.log(obj01.dimensions);
```