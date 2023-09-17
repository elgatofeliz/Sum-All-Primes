# Sum-All-Primes

    JavaScript Algorithms and Data Structures
    Intermediate Algorithm Scripting

Sum All Primes

A prime number is a whole number greater than 1 with exactly two divisors: 1 and itself. For example, 2 is a prime number because it is only divisible by 1 and 2. In contrast, 4 is not prime since it is divisible by 1, 2 and 4.

Rewrite sumPrimes so it returns the sum of all prime numbers that are less than or equal to num.


--- Here's the code ---

function sumPrimes(num) {

  function isPrime(n)
{
    // Check if n=1 or n=0
    if (n <= 1)
        return false;
    // Check if n=2 or n=3
    if (n == 2 || n == 3)
        return true;
    // Check whether n is divisible by 2 or 3
    if (n % 2 == 0 || n % 3 == 0)
        return false;
    // Check from 5 to square root of n
    // Iterate i by (i+6)
    for (var i = 5; i <= Math.sqrt(n); i = i + 6)
        if (n % i == 0 || n % (i + 2) == 0)
            return false;
 
    return true;
}

let result = 0

for (let i = 0; i <= num; i++){
  if(isPrime(i)){
    console.log(i)
    result += i
  }
}
console.log("result", result)
return result
}

sumPrimes(977);
