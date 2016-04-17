The two attached text files are my script for the exercise 1.

For Script memory_check:
  this is my script to manually code the exit in my main script. It calls my main script inside.
  
For Script memory_check_main.txt:
  This is my main script, where it performs items 1 - 3 in exercise 1.
  

sample execution: memory_check.sh -c 90 -w 60 -e weng@apc.com

Sample displays are the ff:

Memory is at 5 % . NORMAL Threshold
Memory is at 5 % . WARNING Threshold
Memory is at 5 % . CRITICAL Threshold

It also email the output to the user with a subject "Memory YYYYMMDD HH:MM memory check status" the subject of the email changes to "Memory YYYYMMDD HH:MM memory check - CRITICAL" if the memory is gretater than or equal to critical threshold and put in the body of the main the top 10 processes (with process ids) that use a lot of memory.

Also uploaded a PDF file for sample out of execution.



  

