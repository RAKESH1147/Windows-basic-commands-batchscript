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

---
## Create a directory named "my-folder"

 __COMMAND AND OUTPUT__

<img width="806" height="79" alt="image" src="https://github.com/user-attachments/assets/a494cf64-7457-44d6-a737-78ee246bf414" />


## Remove the directory "my-folder"

**COMMAND AND OUTPUT**

<img width="866" height="75" alt="image" src="https://github.com/user-attachments/assets/0e84e947-021c-4728-a482-0bd95cf4c5b1" />


## Create the file Rose.txt

**COMMAND AND OUTPUT**

<img width="859" height="73" alt="image" src="https://github.com/user-attachments/assets/5db47aaf-9500-4a86-9aa8-08ff7e7382b9" />


## Create the file hello.txt using echo and redirection

 __COMMAND AND OUTPUT__

<img width="910" height="76" alt="image" src="https://github.com/user-attachments/assets/85f23f43-2e37-4e92-8ce9-46aaf4dc27a2" />


## Copy the file hello.txt into the file hello1.txt

__COMMAND AND OUTPUT__

<img width="933" height="102" alt="image" src="https://github.com/user-attachments/assets/cd2cbfef-b2f0-49aa-8009-065f43232536" />

## Remove the file hello1.txt

 __COMMAND AND OUTPUT__

<img width="802" height="85" alt="image" src="https://github.com/user-attachments/assets/014ce23a-6aa3-4304-9f55-f89238f56017" />


## List out the file hello1.txt in the current directory

 __COMMAND AND OUTPUT__

<img width="832" height="155" alt="image" src="https://github.com/user-attachments/assets/8e5026be-8555-4e12-b1ef-ed039897d9ff" />


## List out all the associated file extensions 

__COMMAND AND OUTPUT__

<img width="742" height="961" alt="image" src="https://github.com/user-attachments/assets/3d06f9ea-a2cf-4c84-b1b1-d0d6bc5a4b95" />

<img width="663" height="962" alt="image" src="https://github.com/user-attachments/assets/83e8563b-10c4-43a1-aed7-d4113b06f9dc" />

<img width="418" height="983" alt="image" src="https://github.com/user-attachments/assets/4893deeb-7896-4caa-b5d9-10f116ddce15" />

<img width="435" height="986" alt="image" src="https://github.com/user-attachments/assets/d943bcf6-9ba6-4da5-997c-ff4092c64011" />

<img width="601" height="988" alt="image" src="https://github.com/user-attachments/assets/2b905870-ff78-41ab-97f7-933e3681e83d" />
<img width="672" height="981" alt="image" src="https://github.com/user-attachments/assets/e3d3d815-ed01-4bad-aa49-94b195a0cdce" />

<img width="542" height="988" alt="image" src="https://github.com/user-attachments/assets/6a600c7b-c298-4c2d-a2fc-42f298fed47f" />

<img width="491" height="983" alt="image" src="https://github.com/user-attachments/assets/f5d4685f-43a0-48f6-9242-d25d37c7d77c" />

<img width="634" height="986" alt="image" src="https://github.com/user-attachments/assets/be0f3bd2-6ded-4a10-b518-d7dffe60823f" />

<img width="591" height="986" alt="image" src="https://github.com/user-attachments/assets/2ed0728f-ee1e-499f-bdb0-3a23d95b38f8" />

## Compare the file hello.txt and rose.txt

 __COMMAND AND OUTPUT__

<img width="886" height="137" alt="image" src="https://github.com/user-attachments/assets/e96d73b9-1f74-4406-b69e-1615ce35b98a" />




## Exercise 2: Advanced Batch Scripting
__1__.Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".

### BATCH PROGRAM

``` batch
@echo off
set name=John
echo Hello, %name%
pause
```



### OUTPUT

<img width="825" height="75" alt="image" src="https://github.com/user-attachments/assets/246a5819-7d58-4422-825d-50d4f3491cc3" />



__2__.Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.

### BATCH PROGRAM
``` batch
@echo off
:loop
set /p num=Enter a number: 
set /a rem=%num% %% 2

if %rem%==0 (
    echo %num% is Even
) else (
    echo %num% is Odd
)

:ask
set /p ans=Do you want to check another number? (Y/N): 
if /I "%ans%"=="Y" goto loop
if /I "%ans%"=="N" goto end
echo Invalid input. Please enter Y or N.
goto ask

:end
echo Thank you!
pause
```

### OUTPUT

<img width="786" height="209" alt="image" src="https://github.com/user-attachments/assets/824ca5c5-27cd-4e9d-ad96-6e8c213fb6e0" />




__3__.Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.

### BATCH PROGRAM

``` batch
@echo off
for /L %%i in (1,1,5) do (
    echo Number: %%i
)
pause
```

### OUTPUT

<img width="867" height="153" alt="image" src="https://github.com/user-attachments/assets/f9c49b25-5767-45b0-9ec3-de8de40ebe4c" />



__4__.Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

__Instructions:__
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):

### BATCH PROGRAM

``` batch
@echo off
if exist sample.txt (
    echo sample.txt exists.
) else (
    echo sample.txt does not exist.
)
pause
```

### OUTPUT

<img width="795" height="75" alt="image" src="https://github.com/user-attachments/assets/f5ebfae9-0b2d-439b-ae29-6cef4ee9c9a2" />


__5__.Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.

### BATCH PROGRAM

``` batch
@echo off
:menu
cls
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
set /p choice=Choose an option (1-3): 

if "%choice%"=="1" goto hello
if "%choice%"=="2" goto create
if "%choice%"=="3" goto exit
echo Invalid choice.
pause
goto menu

:hello
echo Hello, World!
pause
goto menu

:create
echo This is a new file > newfile.txt
echo File newfile.txt created.
pause
goto menu

:exit
echo Goodbye!
pause
exit
```

### OUTPUT

<img width="332" height="126" alt="image" src="https://github.com/user-attachments/assets/349c8a59-0694-4531-9901-98e2f1590f59" />

<img width="304" height="131" alt="image" src="https://github.com/user-attachments/assets/a6f8393b-2c6c-4928-832e-bcb1b0dafe77" />

<img width="307" height="132" alt="image" src="https://github.com/user-attachments/assets/dd439c31-1b0f-47a5-943f-7bc769e8456e" />

# RESULT:
The commands/batch files are executed successfully.

