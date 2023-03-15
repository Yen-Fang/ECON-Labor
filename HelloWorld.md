HelloWorld
================

# Hello, World!

add_numbers \<- function(a, b) { result \<- a + b return(result) }

debug(add_numbers) \# initiate the debugger

add_numbers(2, 3) \# call the function with some arguments

# The debugger will stop at the beginning of the function

# You can press Enter to step through each line of code

# Once you reach the line with the assignment of `result`,

# you can examine its value by typing `result` and pressing Enter

# The debugger will show you the current value of `result`

# To exit the debugger, type `Q` and press Enter
