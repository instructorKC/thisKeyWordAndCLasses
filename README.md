# thisKeyWordAndCLasses



var myButton = {
  content: 'OK',
  click: function click() {
    console.log(this.content + ' clicked');
  }
};

 //myButton.click(); // OK clicked

var looseClick = myButton.click;
 // looseClick(); // not bound, 'this' is not myButton - it is the globalThis

var boundClick = myButton.click.bind(myButton);
// boundClick(); // bound, 'this' is myButton









class Car {
  constructor(name, year) {
    this.name = name;
    this.year = year;
  }

  sayName(){
      return this.name      
  }
}



const vehicle = new Car("toyota1", 1990);
const vehicle2 = new Car("ford", 1995);
// console.log(vehicle);
// console.log(vehicle2);
// console.log(vehicle.sayName());



function Trucks(name, year) {
     this.name = name;
    this.year = year;
}
 Trucks.prototype.getFullName = function () {
   return this.name + ' ' + this.year;
 };

const truck = new Trucks("ford", 1998);
console.log(truck);
 console.log(truck.getFullName());
