# Introduction-to-JavaScript-Arrays
Question solved about Arrays in JavaScript 

## Question 1: UdaciFamily
```
Create an array called udaciFamily and add "Julia", "James", and your name to the array. 
Then, print the udaciFamily to the console using console.log.
```
## Answer 1: 
```
var udaciFamily = ["Julia","James","Sagar"];
 console.log(udaciFamily);
 ```
 ## Question 2: Building the crew 
 ```
 Create an array called crew to organize the Serenity’s crew and set it equal to the variables below . You don't need to type out the actual strings, just use the provided variables.

var captain = "Mal";
var second = "Zoe";
var pilot = "Wash";
var companion = "Inara";
var mercenary = "Jayne";
var mechanic = "Kaylee";
Then, print the crew array to the console.
```
## Answer 2:
```
var crew = ["Mal","Zoe","Wash","Inara","Jayne","Kaylee"];
console.log(crew);
```
## Question 3: The price is right

```
Starting with this array of prices, change the prices of the 1st, 3rd, and 7th elements in the array.

var prices = [1.23, 48.11, 90.11, 8.50, 9.99, 1.00, 1.10, 67.00];
```
```
var prices = [1.23, 48.11, 90.11, 8.50, 9.99, 1.00, 1.10, 67.00];
prices[0] =1.5;
prices[2]= 49;
prices[6]=1.2;



console.log(prices);


```

## Question 4: 
```
James was creating an array with the colors of the rainbow, and he forgot some colors. The standard rainbow colors are usually listed in this order:

var rainbow = ["Red", "Orange", "Yellow", "Green", "Blue", "Purple"];
but James had this:

var rainbow = ["Red", "Orange", "Blackberry", "Blue"];
Using only the splice() method, insert the missing colors into the array, and remove the color "Blackberry" by following these steps:

Remove "Blackberry"
Add "Yellow" and "Green"
Add "Purple"
```
## Answer 4: 
```
var rainbow = ["Red", "Orange", "Blackberry", "Blue"];
rainbow.splice(2,1,"yellow","Green");
rainbow.splice(5,0,"Purple");

console.log(rainbow);
```
## Question 5: Quidditch Cup
```
Consider the following array.

var team = ["Oliver Wood", "Angelina Johnson", "Katie Bell", "Alicia Spinnet", "George Weasley", "Fred Weasley", "Harry Potter"];
Directions:
Create a function called hasEnoughPlayers() that takes the team array as an argument and returns true or false depending on if the array has at least seven players.

Your Code:
```
## Answer 5: 
```
function hasEnoughPlayers(team){
    if(team.length >= 7 ){
        return true;
    }else{
        return false;
    }
    return team;
}

var team = ["Oliver Wood", "Angelina Johnson", "Katie Bell", "Alicia Spinnet", "George Weasley", "Fred Weasley", "Harry Potter"];

console.log(hasEnoughPlayers(team));

```
## Question 6: Joining the crew.

```
In an earlier exercise, you created a crew array to represent Mal’s crew from the hit show Firefly.

var captain = "Mal";
var second = "Zoe";
var pilot = "Wash";
var companion = "Inara";
var mercenary = "Jayne";
var mechanic = "Kaylee";

var crew = [captain, second, pilot, companion, mercenary, mechanic];
Later in the show, Mal takes on three new crew members named "Simon", "River", and "Book". Use the push() method to add the three new crew members to the crew array.

var doctor = "Simon";
var sister = "River";
var shepherd = "Book";
```
## Answer 6: 
```
var captain = "Mal";
var second = "Zoe";
var pilot = "Wash";
var companion = "Inara";
var mercenary = "Jayne";
var mechanic = "Kaylee";

var crew = [captain, second, pilot, companion, mercenary, mechanic];
var doctor = "Simon";
var sister = "River";
var shepherd = "Book";
crew.push(doctor);
crew.push(sister);
crew.push(shepherd);


console.log(crew);
```
## Question 7: Another types of Loops
```
Use the array's forEach() method to loop over the following array and add 100 to each of the values if the value is divisible by 3.

var test = [12, 929, 11, 3, 199, 1000, 7, 1, 24, 37, 4, 19, 300, 3775, 299, 36, 209, 148, 169, 299, 6, 109, 20, 58, 139, 59, 3, 1, 139];
Remember that the "Test Run" button will display any logged content, so feel free to use console.log() to test your code.

Your Code:
```
## Answer 7: 

```
var test = [12, 929, 11, 3, 199, 1000, 7, 1, 24, 37, 4, 19, 300, 3775, 299, 36, 209, 148, 169, 299, 6, 109, 20, 58, 139, 59, 3, 1, 139];

test.forEach(function(value,index){
    if(value % 3 ===0){
        value = value +100;
        test.splice(index,1,value);
    }
})
console.log(test);
```
## Question 8: I Got Bills 
```
Use the map() method to take the array of bill amounts shown below, and create a second array of numbers called totals that shows the bill amounts with a 15% tip added.

var bills = [50.23, 19.12, 34.01, 100.11, 12.15, 9.90, 29.11, 12.99, 10.00, 99.22, 102.20, 100.10, 6.77, 2.22];
Print out the new totals array using console.log.

TIP: Check out the toFixed() method for numbers to help with rounding the values to a maximum of 2 decimal places. Note, that the method returns a string to maintain the "fixed" format of the number. So, if you want to convert the string back to a number, you can cast it or convert it back to a number:

Number("1");
```
## Answer 8:
```
var bills = [50.23, 19.12, 34.01, 100.11, 12.15, 9.90, 29.11, 12.99, 10.00, 99.22, 102.20, 100.10, 6.77, 2.22];

var total = bills.map(function(bill){
    bill = bill + bill*(0.15);
    return Number (bill.toFixed(2));
})
console.log(total);
```
## Question 9: Nested Numbers 
```
Use a nested for loop to take the numbers array below and replace all of the values that are divisible by 2 (even numbers) with the string "even" and all other numbers with the string "odd".

var numbers = [
    [243, 12, 23, 12, 45, 45, 78, 66, 223, 3],
    [34, 2, 1, 553, 23, 4, 66, 23, 4, 55],
    [67, 56, 45, 553, 44, 55, 5, 428, 452, 3],
    [12, 31, 55, 445, 79, 44, 674, 224, 4, 21],
    [4, 2, 3, 52, 13, 51, 44, 1, 67, 5],
    [5, 65, 4, 5, 5, 6, 5, 43, 23, 4424],
    [74, 532, 6, 7, 35, 17, 89, 43, 43, 66],
    [53, 6, 89, 10, 23, 52, 111, 44, 109, 80],
    [67, 6, 53, 537, 2, 168, 16, 2, 1, 8],
    [76, 7, 9, 6, 3, 73, 77, 100, 56, 100]
];
```
## Answer 9: 
```
var numbers = [
    [243, 12, 23, 12, 45, 45, 78, 66, 223, 3],
    [34, 2, 1, 553, 23, 4, 66, 23, 4, 55],
    [67, 56, 45, 553, 44, 55, 5, 428, 452, 3],
    [12, 31, 55, 445, 79, 44, 674, 224, 4, 21],
    [4, 2, 3, 52, 13, 51, 44, 1, 67, 5],
    [5, 65, 4, 5, 5, 6, 5, 43, 23, 4424],
    [74, 532, 6, 7, 35, 17, 89, 43, 43, 66],
    [53, 6, 89, 10, 23, 52, 111, 44, 109, 80],
    [67, 6, 53, 537, 2, 168, 16, 2, 1, 8],
    [76, 7, 9, 6, 3, 73, 77, 100, 56, 100]
];

for (var row=0; row <numbers.length;row++){
    for(var column=0; column<numbers[row].length;column++){
        if(numbers[row][column] % 2 ===0){
            numbers[row][column] = "Even";
        }else{
            numbers[row][column]= "Odd";
        }
    }
}
console.log(numbers);

````
