# day-8-task
a “person” class to hold all the details in javascript

In this class, we have a constructor method that takes in four arguments: name, age, gender, and occupation. These are used to initialize the corresponding properties of the Person object.

class Person {
  constructor(name, age, gender, occupation) {
    this.name = name;
    this.age = age;
    this.gender = gender;
    this.occupation = occupation;
  }
  
  getName() {
    return this.name;
  }
  
  getAge() {
    return this.age;
  }
  
  getGender() {
    return this.gender;
  }
  
  getOccupation() {
    return this.occupation;
  }
  
  setName(name) {
    this.name = name;
  }
  
  setAge(age) {
    this.age = age;
  }
  
  setGender(gender) {
    this.gender = gender;
  }
  
  setOccupation(occupation) {
    this.occupation = occupation;
  }
}

let person1 = new Person("Alice", 30, "Female", "Engineer");

console.log(person1.getName())
console.log(person1.getAge());
console.log(person1.getGender())
console.log(person1.getOccupation());


// Output: "Alice"
// Output: 30
// Output: "Female"
// Output: "Engineer"



class to calculate the uber price

class UberPriceCalculator {
  constructor(distance, surgeMultiplier, serviceFee) {
    this.distance = distance;
    this.surgeMultiplier = surgeMultiplier;
    this.serviceFee = serviceFee;
    this.baseFare = 2.50;
    this.costPerMile = 1.50;
    this.costPerMinute = 0.20;
  }

  calculatePrice() {
    const distanceCost = this.distance * this.costPerMile;
    const timeCost = 10 * this.costPerMinute;
    const subtotal = this.baseFare + distanceCost + timeCost;
    const surgePrice = subtotal * this.surgeMultiplier;
    const totalCost = surgePrice + this.serviceFee;

    return totalCost.toFixed(2);
  }
}

// Example usage
const distance = 10; // in miles
const surgeMultiplier = 1.5; // 50% surge
const serviceFee = 1.50; // flat fee

const calculator = new UberPriceCalculator(distance, surgeMultiplier, serviceFee);
const price = calculator.calculatePrice();
console.log(price); // Output: "25.75"
