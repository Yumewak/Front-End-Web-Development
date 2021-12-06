# Front-End-Web-Development
## Snippets
### BMI Calculator
    //Create your function below this line.

    //The first parameter should be the weight and the second should be the height.

    function bmiCalculator(weight, height){

    var bmi = Math.round(weight/Math.pow(height, 2));

    return bmi; //here also can be "return Math.round(bmi);" instead of Math.round in the 4 line

    }

    var bmi = bmiCalculator(65, 1.8);

    console.log (bmi);

    /\* If my weight is 65Kg and my height is 1.8m, I should be able to call your function like this:

    var bmi = bmiCalculator(65, 1.8);

    bmi should equal 20 when it's rounded to the nearest whole number.

    \*/

## Love Calculator
prompt ("Whats your name?")
     
     prompt ("Whats their name?")
     
     var loveScore = Math.random() * 100 //originali Math.floor(Math.random()*101)
     
     loveScore = Math.floor(loveScore) + 1
     
     alert ("Your love score is " + loveScore + "%")

## Random Number
    var n = Math.random();
     
     n=Math.floor((n*6)+1); //also works "n=n*7" and in the next line "n=Math.floor(n)" also we add 1 to simulate the dice roll
     
     console.log(n);

## Control Statements
    var loveScore = Math.random() * 100 //originali Math.floor(Math.random()*101)

    loveScore = Math.floor(loveScore) + 1

    if (loveScore > 70){

    alert ("Your love score is " + loveScore + "%. You love each other like Kanye loves Kanye")
    
    }else {

    alert ("Your love score is " + loveScore + "%")
    
    }
    
## Comparators and Equality
    var a = "1"
    var b = 1
    if (a==b){ //=== This also checking data types wheras == It doesn't care data types
    console.log("Its Equal")
    }else{
    console.log("Its not Equal")
    }
    /* Here is a list of comparators
    ==   Is equal to "Doesn't care data types"
    ===  Is equal to "This also check data types"
    !=== Is not equal to
    <    Is lesser than 
    >    Is greater than
    <=   Is lesser or equal to
    >=   Is greater or equal to
    */

## Combining Comparators
    // var loveScore = Math.floor((Math.random() * 100)+1)
    // if (love > 70){
    //     console.log (love + "% Your love is great")
    // }else{
    //     if (loveScore > 30 && loveScore <= 70){
    //         console.log (loveScore)
    //     }else {
    //         console.log (loveScore + "% Your love is dark")
    //     }
    // }
    
    //This is how whas solved in the course
    
    var loveScore = Math.random() * 100 //originali Math.floor(Math.random()*101)
    loveScore = Math.floor(loveScore) + 1
    
    if (loveScore > 70){
    alert ("Your love score is " + loveScore + "%. You love each other like Kanye loves Kanye.")
    }

    if (loveScore > 30 && loveScore <= 70){
    alert ("Your love score is " + loveScore + "%")
    }
    
    if (loveScore <= 30){
    alert ("Your love score is " + loveScore + "% You go together like oil and water.")
    }

## Leap Year
    // function isLeap(year) {
        
    // /**************Don't change the code above****************/    
        
    //     //Write your code here.    
    // if ((year / 4) % 1 === 0){
    //     if ((year / 100) % 1 === 0){
    //         if ((year / 400) % 1 === 0){
    //             return "Leap year."
    //         }else{
    //             return "Not leap year."
    //         }
    //     }else{
    //         return "Leap year."
    //     }
    // }else{
    //     return "Not leap year."
    // }
    // /**************Don't change the code below****************/    
    
    // }
    
    function isLeap(year) {
    
    /**************Don't change the code above****************/    
        
    //Write your code here.    
    if (year % 4 === 0){
    if (year % 100 === 0){
        if (year % 400 === 0){
            return "Leap year."
        }else{
            return "Not leap year."
        }
    }else{
        return "Leap year."
    }
    }else{
    return "Not leap year."
    }
    /**************Don't change the code below****************/    
    
    }
    isLeap(2999)

## Collections, Working with arrays
    var guestList = ["Angela", "Jack", "Pam", "James", "Lara", "Jason"]
    var guestName = prompt ("What is your name?")
    if (guestList.includes(guestName)){
        alert ("Welcome!.")
    }else{
        alert("Sorry maybe next time.")
    }

## Adding Elements and Intermidiate Array Technique
    var output = []
    var count = 1
    function fizzBuzz(){
        if (count % 3 === 0 && count % 5 === 0){
            output.push("FizzBuzz")
        }
        else if (count % 3 === 0) {
            output.push("Fizz")
        }
        else if (count % 5 === 0){
            output.push("Buzz")
        }
        else{
            output.push(count)
        }
        count++
        console.log(output)
    }
    
    
    
    
    
    
    // var output = []
    // var count = 1
    // function fizzBuzz(){
    //         output.push(count)
    //     if (count%3 === 0 && count%5 === 0) {
    //         output.pop()
    //         output.push("fizzBuzz")
    //     }else{
    //         if (count%3 === 0){
    //             output.pop()
    //             output.push("fizz")
    //         }else{
    //             if (count%5 === 0){
    //                 output.pop()
    //                 output.push("buzz")
    //             }
    //         }
    //     }
    //     console.log(output)
    //     count++
    // }

## Who's buying lunch
    //You call this function with whosPaying() and the other one below whosPaying([])
    function whosPaying(names) {
        
    /******Don't change the code above*******/
        
        //Write your code here.
        var list = ["Angela", "Ben", "Jenny", "Michael", "Chloe"]
        var random = Math.floor(Math.random() * (list.length))
        var name = list[random]
        return name + " is going to buy lunch today!"
    
    
    /******Don't change the code below*******/    
    }

    // Write a function wich will select a random name from a list of names. 
    // The person selected will have to pay for everybody's food bill.
    
    // Example Input
    // ["Angela", "Ben", "Jenny", "Michael", "Chloe"] // Remember use "[]", when call the function use whosPaying([])
    // Example Output
    // [Michael is going to buy lunch today!]
    // Input a diferent name each time you call the whosPaying function and it will riturn a random name from the list
    
    // function whosPaying(names) {
    
    //     var numberOfPeople = names.length
    //     var randomPersonPosition = Math.floor(Math.random() * numberOfPeople)
    //     var randomPerson = names[randomPersonPosition]
    
    //     return randomPerson + " is going to buy lunch today!"
    // }

## Control Statements While Loops
    var output = []
    var count = 1
    function fizzBuzz(){
        while (count <= 100){
        if (count % 3 === 0 && count % 5 === 0){
            output.push("FizzBuzz")
        }
        else if (count % 3 === 0) {
            output.push("Fizz")
        }
        else if (count % 5 === 0){
            output.push("Buzz")
        }
        else{
            output.push(count)
        }
        count++
        //console.log(output)if we put the output here then it will print a hundred times the numbers till one hundred
        }
        console.log(output) // if we put the output here then it will print one time the numbers till one hundred
    }

## 99 Bottles of beer
    var count = 99
    function beer(){
        while (count > 1) {
            console.log (count + " bottles of beer on the wall, " + count + " bottles of beer.")
            count --
            console.log ("Take one down and pass it around, " + count + " bottles of beer on the wall.")
        }
        console.log ("1 bottle of beer on the wall, 1 bottle of beer.")
        console.log("Take one down and pass it around, no more bottles of beer on the wall.")
        console.log("No more bottles of beer on the wall, no more bottles of beer.")
        console.log("Go to the store and buy some more, 99 bottles of beer on the wall.")
    }
    
    // function cheers(){
    //     var count = 100;
    //     while(count>2) {
    //        count--;
    //        console.log(count + " bottles of beer on the wall, " + count + " bottles of beer. Take one down and pass it around, " + (count-1) + " bottles of beer.");
    //     }
 
    //     count[1] = console.log("1 bottle of beer on the wall, 1 bottle of beer. Take one down and pass it around, 1 bottle of beer.");
    //     count[0] = console.log("No more bottles of beer on the wall, no more bottles of beer. Go to the store and buy some more, 99 bottles of beer. Cheers :-)!");     
    // }

## Control Statements For Loops
    var output = []
    function fizzBuzz(){
        for (var count = 1; count <= 100; count++){
        if (count % 3 === 0 && count % 5 === 0){
            output.push("FizzBuzz")
        }
        else if (count % 3 === 0) {
            output.push("Fizz")
        }
        else if (count % 5 === 0){
            output.push("Buzz")
        }
        else{
            output.push(count)
        }
        //console.log(output)if we put the output here then it will print a hundred times the numbers till one hundred
        }
        console.log(output) // if we put the output here then it will print one time the numbers till one hundred
    }
    
## Fibbonacci 01 This is how i've solved
    function fibonacciGenerator (n) {
        var array = []
        var number = 0
        for (var count = 0; count < n; count ++){
                array.push(number)
                if (number === 0){
                    number++
                }else{
                    number = number + array[count-1] 
                }
        }
        return array
    }
    fibonacciGenerator(10)
    
## Fibonnaci 02 This is how whas solved in the course
    function fibonacciGenerator (n) {
    //Do NOT change any of the code above 👆
        
        //Write your code here:
        var output = []
        if (n === 1){
            output = [0]
        }
        else if (n === 2){
            output = [0,1]
        }
        else {
            output = [0,1]
             for (var i = 2; i<n; i++){
                 output.push(output[output.length - 2] + output[output.length - 1])
             }
            }
        return output
        //Return an array of fibonacci numbers starting from 0.
        
    //Do NOT change any of the code below 👇
    }
    fibonacciGenerator(8)
    
## Fibonacci 03 This is how a student in the chat solved
    function fibonacciGenerator (n) {
    
        var fib  = [0,1];
    
        for(var i = 0; i < n; i++){
    
        
    
          fib.push((fib[i+0]) + (fib[i+1]));
    
        }
    
        return fib
    
    }

## Higer oder function
    function add(num1, num2) {
    return num1 + num2;
    }
     
    function subtract(num1, num2) {
    return num1 - num2;
    }
     
    function multiply(num1, num2) {
    return num1 * num2;
    }
     
    function divide(num1, num2) {
    return num1 / num2;
    }
     
    function calculator(num1, num2, operator) {
    return operator(num1, num2);
    }

## JavaScript Objects
    //alert("Hello, my name is " + bellBoy1Name)
    var bellBoy1Name = "Timmy";
    var bellBoy1Age = 19;
    var bellBoy1HasWorkPermit = true;
    var bellBoy1Languages = ["French","English"];
    
    //alert("Hello, my name is " + bellBoy1.name)
    var bellBoy1 = {
        name: "Timmy",
        age: 19,
        hasWorkPermit: true,
        languages: ["French", "English"]
    }
    
    //Constructor Function, names have to be capitalized, the first letter of the first word also has to be capitalized
    function BellBoy (name, age, hasWorkPermit, languages){
        this.name = name;
        this.age = age;
        this.hasWorkPermit = hasWorkPermit;
        this.languages = languages;
    }
    
    //Initialise Object
    var bellBoy1 = new BellBoy("Timmy", 19, true, ["French", "English"])
