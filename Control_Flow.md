# Control Flow

    Very often in computer programming, you will find yourself needing to only execute code under certain conditions or you need to excecute code multiple times. This is where control flow comes into play. Python's control flow statements are very similar to the ones that you would see in other languages, but there are some key differences that I will mention later. Before we get into control flow statements, it is a good idea to cover some operators that are often used with if statements.

## Comparison Operators

    In all programming languages, there are a list of boolean operators that determine whether two values are equal to eachother, or if one value is greater than another. Here is a list of boolean operators in Python:

        == : checks to see if both objects are equal to one another
            ex: 2 == 2 evaluates to True

        != : checks to see if both objects are not equal to one another
            ex: 2 != 2 evaluates to False

        < : checks if value before operator is less than the value after the operator
            ex: 1 < 3 evaluates to True

        > : checks if value before operator is greater than the value after the operator
            ex: 3.5 > 2.5 evaluates to True

        <= : checks if value before operator is less than or equal to the value after the operator
            ex: 2.2 <= 4.7 evaluates to True

        >= : checks if value before operator is greater than or equal to the value after the operator
            ex: 2.2 >= 2.2 evaluates to True

    There are more comparison operators, but since they involve topics not yet discussed, they will be referenced in their respective chapters.

## if-elif-else statements

    The if statement is used to conditionally execute certain blocks of code if the contional part evaluates to True, then the block of code is executed, otherwise, the execution context continues past the if statement. The common syntax in Python is this:

        `
            if {condition}:
                do stuff
            {exit the if block}
        `

    Since Python does not use {} to determine code blocks, you distinguish the code in an if statement with a tab or space. It is feasible to have multiple if statements to have different execution blocks for different conditions:

        `
            if {condition}:
                do stuff
            if {other condition}:
                do something else
            {exit the if blocks}
        `

    This would work, but often if you have related if statements, it is best to use an else if in order to both show that the if statements are connected, and to pass over them if one of the conditions is evaluated to true. In Python, the else if condition is shortened to elif. Here is how it is used:

        `
            if {condition}:
                do stuff
            elif {other condition}:
                do something else
            {exit the if blocks}
        `

    Like other languages, Python allows for just an else statement in order to have a code block that executes if nothing else does. 

            `
                if {condition}:
                    do stuff
                else:
                    do something else
                {exit the if blocks}
            `

## Boolean Operators

    Often times you will want to have other conditions in an if statement. There are a number of boolean operators that change the behavior of the statement. It is worth noting that other languages have these kind of operators, but Python's boolean operators are a little different then most other languages. Here is a listing:

        not : this will negate the condition that is evaluated after it. for example, `not True` will evaluate to False. Equivalent to the ! operator.

        and : this will take two conditional expressions and evaluate them to True if both of those conditions evaluates to True. Equivalent to the && operator.

        or : this will take two conditional expressions and evaluate them to True if one of those conditions evaluates to True. Equivalent to the || operator.

## Switch Statement in Python

    Python does not actual have a switch statement, however, there is a way to implement a switch statement in Python using a dictionary, but because it has not been covered yet, this crash course will skip this and cover it in the section for Python collections.

## While Statement

    The while statement will loop over a section of code continually until the condition after the while keyword. Because a while statement only contains a condition within its declaration, it is vital to have some way of changing the variable that is bring changed within it. Example:

        `
            x = 0
            while x == 0:
                pass
        `
        note: pass is a keyword in Python that does nothing. It is useful if you want to create a function or loop without doing anything with it initially.

    The problem with the above code is that it will never exit. In the event that you accidentally create an infinite loop, doing CTRL+C will kill that process so that you can go back in your code and check why the loop is continuing infinitely.

## Range Function

    This is not technically a part of Python's control flow, but it is very helpful to know. Range is a function that will return an iterable object using the given integer values. There are three parameters for the function, two of them are optional. The first is where the iterable should start, by default it starts at the number 0. The second is which number to stop at, there is no default here and it is also important to note that the loop will execute the number before this. The last number is the number to step by, the default here is 1. Here is an example of the function:

    `
        range(0, 10, 2)
    `

    In this example, the numbers 0, 2, 4, 6, and 8 are returned. Note that if you surround this in a print statement, it will print "range(0, 10, 2)" instead of a listing of 0, 2, 4, 6, 8. To actually get it to print these numbers, you would have to do this:

    `
        print(list(range(0, 10, 2)))
    `

    What happens here is that because the range function returns an iterable object, you can convert it to a list, where it then is converted to something more readable, i.e. [0, 2, 4, 6, 8]

## For Statement

    A for loop is very similar to the while loop, except that instead of only having a condition within its declaration, there is a condition, an increment, and an initialization within its declaration. An example:

        `
            for i in range(5):
                do stuff
        `
    
    What happens here is that Python will iterate over a range of numbers (in this case, 0-4) and exit when it is done. For loops in Python iterate over some kind of sequential object. This will be discussed more in the section on structures.

## Other Important Statements

    Python has some other statements that help control the flow of a loop. Here is a listing of them:

        break : this will exit a loop that it is inside (if inside a nested loop, it will not break out of the outer loop, just the loop that the break statement is inside)

        continue: this will continue to the next iteration of the loop. any code after the call to continue will not execute during the iteration on which the continue statement is called.

        else: You can put in an else statement after a for statement to have it execute when the condition in the for/while statement evaluates to False. The else statement will not execute if the previous loop exited from a break statement.

    

