# Windows-basic-commands-batchscript
Ex08-Windows-basic-commands-batchscript

# AIM:
To execute Windows basic commands and batch scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware 

### Step 2:

Write the Windows commands / batch file . Save each script in a file with a .bat extension. Ensure you have the necessary permissions to perform the operations. Adapt paths as needed based on your system configuration.
### Step 3:

Execute the necessary commands/batch file for the desired output. 




# WINDOWS COMMANDS:
## Exercise 1: Basic Directory and File Operations
Create a directory named "my-folder"

## COMMAND AND OUTPUT
<img width="887" height="111" alt="image" src="https://github.com/user-attachments/assets/4286b51a-cee7-4810-93d6-b3a0cfede39b" />

Remove the directory "my-folder"

## COMMAND AND OUTPUT

<img width="911" height="55" alt="image" src="https://github.com/user-attachments/assets/d74ba5df-9c89-485d-904f-7a404682bddf" />

Create the file Rose.txt

## COMMAND AND OUTPUT

<img width="767" height="107" alt="image" src="https://github.com/user-attachments/assets/0fc42efd-f38e-4613-b668-8efffe545e83" />

Create the file hello.txt using echo and redirection

## COMMAND AND OUTPUT
<img width="819" height="107" alt="image" src="https://github.com/user-attachments/assets/a976c61c-d359-46e5-8ef6-11e19b471959" />

Copy the file hello.txt into the file hello1.txt

## COMMAND AND OUTPUT
<img width="671" height="62" alt="image" src="https://github.com/user-attachments/assets/4e9412f5-298d-46ce-ac55-76fc24b974f5" />

Remove the file hello1.txt

## COMMAND AND OUTPUT
<img width="658" height="171" alt="image" src="https://github.com/user-attachments/assets/d9e4271f-f442-462f-874a-daece1ce36cb" />

List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT
<img width="658" height="171" alt="image" src="https://github.com/user-attachments/assets/55c37ab9-f8b7-4bcd-8abe-2d3ecf8a095b" />

List out all the associated file extensions 

## COMMAND AND OUTPUT

<img width="574" height="613" alt="image" src="https://github.com/user-attachments/assets/e39c6f23-6469-4d05-abee-a445fc6d187a" />

Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT
<img width="614" height="218" alt="image" src="https://github.com/user-attachments/assets/e71be7a2-f2fd-451e-bc1e-14cbc99854fa" />

## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".
~~~
@echo off
set name=John
echo Hello, %name%!
pause
~~~




## OUTPUT

<img width="506" height="80" alt="image" src="https://github.com/user-attachments/assets/045b5c2d-3d26-42c8-bbe6-93df0904db8a" />


Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.
~~~
@echo off
:main
set /p number=Enter a number: 
rem Calculate remainder when divided by 2
set /a remainder=%number% %% 2
if %remainder%==1 (
    echo %number% is an odd number.
) else (
    echo %number% is not an odd number.
)
:choice
set /p continue=Do you want to check another number? (Y/N): 
if /i "%continue%"=="Y" goto main
if /i "%continue%"=="N" goto end
echo Invalid choice, please enter Y or N.
goto choice
:end
echo Thank you for using the odd number checker!
pause
~~~


## OUTPUT


<img width="664" height="159" alt="image" src="https://github.com/user-attachments/assets/e85a0b3c-389c-4192-b8f2-a772c3e966ae" />


Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.

~~~
@echo off
for %%i in (1 2 3 4 5) do (
    echo Number: %%i
)
pause
~~~


## OUTPUT

<img width="550" height="204" alt="image" src="https://github.com/user-attachments/assets/c4efefe8-ae2a-4f56-831f-43d7eaaa8249" />



Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):
~~~
@echo off
if exist sample.txt (
    echo sample.txt exists.
) else (
    echo sample.txt does not exist.
)
pause
~~~

## OUTPUT
<img width="488" height="80" alt="image" src="https://github.com/user-attachments/assets/17278ad2-109e-417d-bbe5-556106173178" />
~~~
@echo off
:menu
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
set /p choice=Choose an option: 
if "%choice%"=="1" goto hello
if "%choice%"=="2" goto createfile
if "%choice%"=="3" goto end

:hello
echo Hello, World!
goto menu

:createfile
echo Creating a file...
echo This is a new file > newfile.txt
goto menu
:end
echo Goodbye!
pause
~~~

Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.


## OUTPUT

<img width="466" height="298" alt="image" src="https://github.com/user-attachments/assets/36d1b673-3556-46a1-a541-9a5033e06ecc" />


# RESULT:
The commands/batch files are executed successfully.

