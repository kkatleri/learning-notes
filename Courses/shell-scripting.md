# Shell Scripting

- [Notes](#notes)
- [Syntax](#syntax)
- [Unix Concepts](#unix-concepts)
- [Unix Commands](#unix-commands)

## Notes
- Helps automate repetative manual tasks
- Shell scripts by default do not have execute permission, hence its executed using bash command
- To execute on its own, give it execute permission using chmod command
- Comments begin with '#' sign


## Syntax
- Printing
    - echo command
- Comments
    - Use '#' sign at the start of the line
- Shebang (#!)
    - Scripts needs to be excuted using right command processor
    - bash is the one for shell scripts
    - Generally bash is the default shell in most of the unix system
    - Shebang allows you to explicitely declare shell for your script
    - Syntax
        - #!/usr/bin/env bash
    - Examples
        - #!/usr/bin/env bash (For shell scripts)
        - #!/usr/bin/env python (For python scripts)
        - #!/usr/bin/env node (For Javascripts)
- Variables
    - VAR_NAME=var_value
    - no space on either side of =
    - Good practice to use variable name in uppercase
    - If the value has space in it, surround it with single or double quote.
- Passing parameters
    - Parameters can be passed to the script from outside while executing script
    - makes it dynamic script
    - By default Bash passes one paramter i.e name of the file including path
    - Parameters are accessed inside the script using $ sign
    - $0 - name of the file including path
- Exit code
    - All the shell scripts return exit code 
    - 0 is success, anything else usually indicates error
    - it ranges 0-255
- Conditional
    - if-then-fi
    - if-then-else-fi
    - if-then-elif-then-else-fi
- Looping
    - while do-done
    - for in do-done
    - flow control
        - break - breaks the loop
        - continue - goes to top of the loop, gets next element to process
 - Funtions
    - funtion funtion_name(){}
    - funtion_name(){}
    - Scripts are executed sequentially from top to bottom
    - so funtion should be defined first before its called
    - Calling a funtion: funtion-name   
    - Passing parameter to a funtion is same as passing em to script and accessed using $1, $2 etc
    - Declare local variable
        - local keyword
    - If not declared local, its global by defauly meaning another funcion in the same script can access that variable
    - Piping
        - Superpower of unix
        - Helps you pass output of command as input to other
        - e.g ls -1 | sort | Head -3
        - Using piping in scripts
            - Using backticks `ls -l | sort -r | head -3`
- File operations
    - Reading a file
        - Using redirection '<' operator
    - Writing a file
        - Using redirection '>' operator
        - '>' overwrites a file
        - '>>' appends to a file
- Putting process to sleep
    - sleep command
- User input
    - read command 
    - e.g read -p "message : " VAR_TO_HOLD_INPUT



## Unix Concepts
- File permission in Unix
    - represented as series of letters and symbols
    - 10 characters
    - First character denotes type of file
        - '-' means regular file
        - 'd' means directory
        - 'l' means symbolic link
    - Remaining 9 characters denotes file permissions for 3 categories of users
        - rwx-rwx-rwx
        - first set is Owner, next set is for Group members and last is for others
        - this is also represent as numbers
        - r=4, w=2, x=1
        - so rwx-r-x-r-x = 755

## Unix Commands
- touch <filename>
    - creates a new file if it does not exist
    - Updates the timestamp if exists
- echo <content>
    - prints content on the console
- bash <shell-script>
    - executes shell scripts
- chmod <permission>
    - Changes file permission as given
    - e.g - chmod 755 : Provides execute permission
- ps 
    - lists all running processes
- sleep <duration>
    - puts process to sleep for duration


