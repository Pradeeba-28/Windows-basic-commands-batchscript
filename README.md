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
Remove the directory "my-folder"
<br>
<img width="780" height="136" alt="image" src="https://github.com/user-attachments/assets/cfe5440a-8d7d-438a-bc9b-f7589d6bd17d" />

## COMMAND AND OUTPUT
Create the file Rose.txt
<br>
<img width="962" height="367" alt="image" src="https://github.com/user-attachments/assets/fafead9b-cc6d-4a45-a6b0-682e62923f5d" />



## COMMAND AND OUTPUT
Create the file hello.txt using echo and redirection
<br>
<img width="890" height="120" alt="image" src="https://github.com/user-attachments/assets/fa57b227-742c-40aa-8f94-15308d892589" />


## COMMAND AND OUTPUT
Copy the file hello.txt into the file hello1.txt
<br>
<img width="917" height="146" alt="image" src="https://github.com/user-attachments/assets/f0281234-4542-418f-9c19-9bc7678fb8cf" />


## COMMAND AND OUTPUT
Remove the file hello1.txt
<br>
<img width="891" height="236" alt="image" src="https://github.com/user-attachments/assets/3550b302-99ac-4a13-9d77-59646acee262" />


## COMMAND AND OUTPUT
List out the file hello1.txt in the current directory
<br>
<img width="579" height="181" alt="image" src="https://github.com/user-attachments/assets/0a915878-9679-470b-b6d2-e9e37b363787" />


## COMMAND AND OUTPUT
List out all the associated file extensions 
<img width="856" height="912" alt="image" src="https://github.com/user-attachments/assets/152a0676-7f27-4e58-9657-591ce601d365" />


## COMMAND AND OUTPUT
Compare the file hello.txt and rose.txt
<img width="726" height="222" alt="image" src="https://github.com/user-attachments/assets/74d123ba-3dce-4d2a-a01c-c63ef0ffd8d0" />


## COMMAND AND OUTPUT

## Exercise 2: Advanced Batch Scripting
## Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".
```
@echo off
set name=John
echo Hello, %name%!
pause
```

## OUTPUT
<img width="623" height="95" alt="image" src="https://github.com/user-attachments/assets/b3b1625c-0894-47ce-bfe9-f2c0cc6466fd" />

## Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
1. Prompt the user to enter a number.
2. Calculate the remainder when the number is divided by 2.
3. Display whether the number is odd or not.
4. Ask the user if they want to check another number.
5. Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
6. Handle invalid inputs for the continuation prompt (Y/N) gracefully.

```
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
```

## OUTPUT
<img width="861" height="241" alt="image" src="https://github.com/user-attachments/assets/7420e67d-511a-46cb-96d7-e7523b539cee" />


## Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.
```
@echo off
for %%i in (1 2 3 4 5) do (
    echo Number: %%i
)
pause
```

## OUTPUT
<img width="748" height="184" alt="image" src="https://github.com/user-attachments/assets/c9aa7831-73a6-46be-9c13-f72cdae0c460" />


## Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):
```
@echo off
if exist sample.txt (
    echo sample.txt exists.
) else (
    echo sample.txt does not exist.
)
pause
```

## OUTPUT
<img width="905" height="228" alt="image" src="https://github.com/user-attachments/assets/1aa26121-3258-40c7-817a-e704a3945191" />


## Write a batch script that displays a simple menu with three options:
1. Say Hello – Displays the message Hello, World!
2. Create a File – Creates a file named newfile.txt with the content This is a new file
3. Exit – Exits the script with a goodbye message
4. The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.

```
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
```
## OUTPUT
<img width="707" height="423" alt="image" src="https://github.com/user-attachments/assets/f17482d2-976a-48af-975a-994ef3919e48" />


# RESULT:
The commands/batch files are executed successfully.

