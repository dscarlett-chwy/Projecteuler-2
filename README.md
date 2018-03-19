# Projecteuler-2

Problem: Each new term in the Fibonacci sequence is generated by adding the previous two terms. By starting with 1 and 2, the first 10 terms will be:
1, 2, 3, 5, 8, 13, 21, 34, 55, 89, ...
By considering the terms in the Fibonacci sequence whose values do not exceed four million, find the sum of the even-valued terms.

Solution:
var x = 0;
var y = 1;
var next =1;
sum = 0
function fib(){

while(next <= 4000000){
  next = x +y;
  x = y;
  y = next;
  if(next%2 === 0){
    sum += next;
  }
}
console.log(sum)
}
fib()

Explained:
SO with this problem I decided to make 3 variabes x, y, sum, and next. I did this so I could run the fibonacci effect. Now I needed a function to be able to run the fibonacci sequence which outputs dont exceed 4 million. Then I needed to target all my even outputs and add them together so I made an if statement to get all numbers that are divisable by 2 with no remainder and add those numbers to my sum variable. Finally I called my function fib() which produce the answer 4613732.
