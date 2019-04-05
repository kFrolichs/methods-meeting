# Coding standards
[Suggested coding standards](https://www.ee.columbia.edu/~marios/matlab/MatlabStyle1p5.pdf)

# Some to take into consideration

## Variables
The names of variables should document their meaning or use.
Especially for large scope variables.
- Use of **camelCase**

- Iterator variables prefixed by i or j
- Avoid using keywords or special values
	Command 'iskeyword' to check

## Structures	
Structures should begin with capital letter

## Functions
The names of functions should document their use.

- It is clearest to have the function and its m-file names the same. Using lower case avoids potential filename problems in mixed operating system environments.
- Functions should have meaningful names!
```matlab
Use computetotalwidth()
Avoid compwid()
```
	
- Abbreviations in names should be avoided. Using whole words reduces ambiguity and helps to make the code self-documenting.
```matlab
Use computearrivaltime(.)
Avoid comparr(.)
```

## Loops
Loop variables should be initialized immediately before the loop.
This improves loop speed and helps prevent bogus values if the loop does not execute for all
possible indices.
```matlab
result = zeros(nEntries,1);
for index = 1:nEntries
	result(index) = foo(index);
end
```

## Comments
The purpose of comments is to add information to the code. Typical uses for comments are to
explain usage, provide reference information, to justify decisions, to describe limitations, to
mention needed improvements. Experience indicates that it is better to write comments at the
same time as the code rather than to intend to add comments later.

## Avoid cryptic code
>Martin Fowler: “Any fool can write
>code that a computer can understand. Good programmers write code that humans can
>understand.” 

>Kreitzberg and Shneiderman: “Programming can be fun, so can cryptography;
>however they should not be combined.”
	
## Files and Organization
The best way to write a big program is to assemble it from well designed small pieces (usually
functions). This approach enhances readability, understanding and testing by reducing the amount
of text which must be read to see what the code is doing. Code longer than two editor screens is a
candidate for partitioning. Small well designed functions are more likely to be usable in other
applications.

