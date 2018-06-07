# R101
R101
 this video, we're going to show you how to work with functions in the R programming
language.
A function is a block of code that can be re-used in different parts of a program.
Generally speaking, this can be broken down into pre-defined functions, and user-defined
functions.
Pre-defined functions are the functions that are already defined for you, whether they're
built in to R or provided in a separate package.
Let's take a look at a few common functions.
Here, we define a small vector of movie ratings, and we use the built-in "mean" function to
find the average, which you can see in the output.
The "sort" function is used to order the elements of a vector.
Notice that the elements are arranged in ascending order.
This is the default behavior.
If you'd like to sort in descending order, you need to add the parameter "decreasing
= TRUE" when calling the function.
As we mentioned, you can define your own functions as well.
In this code snippet, we create a function called "printHelloWorld" that, when run, simply
prints "hello world" to the screen.
So if we call this function by name, we get the expected output.
Our functions can take in arguments as well.
The "add" function here takes in two numbers, and produces the sum as output.
The "return" statement can be used to explicitly output a value from the function.
When "return" is encountered, anywhere in the function, the corresponding value will
be output and the function will exit.
Keep in mind that if the function lacks a return statement, then R will automatically
return the value of the last evaluated expression.
The "return" statement is particularly useful when you need an "if else" block, since the
final output value will be dependent on some condition.
Take a look at the function "isGoodRating" that we've defined.
This function takes in a movie rating and runs through a conditional block.
So the function will return a different value depending on the input.
For example, if we pass in 6, the "if" statement will be "true" and "NO" will be returned.
But if we pass in 9.5, the "if" statement will be false and the function will return
"YES" inside the "else" block.
If you wish, you can set a default value for a function argument.
Notice in the function definition we've added "threshold = 7".
Now when we call this function, we only need to specify the "rating" parameter.
R will automatically use the value of 7 for threshold.
However, you can also override the default value, like so.
Now since 8 is less than the specified value of 8.5, the function will return "NO" as its
output.
To increase the complexity of an application, you can use functions within other functions.
Let's first see the main function we're going to build at a high level.
The function will receive a movie name and a threshold, and it will determine whether
to watch the movie by outputting "YES" or "NO".
In order to do this, the function will check a database for the movie's average rating.
This rating, along with the default threshold of 7, will be passed to the previously defined
"isGoodRating" function.
The final output of the function will depend on the output of "isGoodRating".
So based on the dataset you see here, let's take a look at the entire function's structure.
The function is called "watchMovie", and it takes in the movie's name, as well as a rating
threshold.
This line is responsible for pulling the movie's rating from the database.
It does this by finding a matching name in the "name" column, and then finding the "average
rating" value in the corresponding row.
In the next line of the function, we pass this rating to the "isGoodRating" function.
"my threshold" is passed as well, but it has the same default value of 7.
So if we pass in the movie name "Akira", the rating is 8.1, which is greater than the default
threshold of 7.
So the output will be "YES".
We can also override the threshold, but 8.1 is still greater than 8, so once again we
get "YES" as output.
Variables can be defined inside of functions, but there are a few important considerations.
The function here, when run, will simply output "hello world".
But take a closer look at the variables "y" and "temp".
If you try to access "y" outside of the function, you'll notice the output is 3.14.
But if you try to access "temp", we get an error instead.
This is because there is a difference in how these variables are defined.
You'll notice that "temp" uses the standard variable assignment operator, but the operator
for "y" has an extra "left arrow".
This means that "y" is defined as a global variable, so it can be accessed outside the
function.
"temp" on the other hand is local, so it can only be accessed inside the function.
By now, you should understand how to work with both pre-defined and user-defined functions,
how to nest functions within other functions, and how to create global variables.
Thank you
