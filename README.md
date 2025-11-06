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

<img width="677" height="87" alt="image" src="https://github.com/user-attachments/assets/a7792f2b-e1b4-4d55-97fc-e5422b5b1a88" />



## Remove the directory "my-folder"

**COMMAND AND OUTPUT**

<img width="717" height="75" alt="image" src="https://github.com/user-attachments/assets/268a39ab-341c-43bf-b9f7-ed6cff8a6ae5" />



## Create the file Rose.txt

**COMMAND AND OUTPUT**

<img width="766" height="67" alt="image" src="https://github.com/user-attachments/assets/5bc8200e-6269-4d8a-8cf5-07d72614d9ac" />



## Create the file hello.txt using echo and redirection

 __COMMAND AND OUTPUT__

<img width="638" height="77" alt="image" src="https://github.com/user-attachments/assets/cd7fe78a-9d1d-45ca-a7a5-a42391d813e0" />


## Copy the file hello.txt into the file hello1.txt

__COMMAND AND OUTPUT__

<img width="622" height="95" alt="image" src="https://github.com/user-attachments/assets/224582ab-bd1b-4268-bc3d-74d8209198ef" />

## Remove the file hello1.txt

 __COMMAND AND OUTPUT__

<img width="418" height="67" alt="image" src="https://github.com/user-attachments/assets/347e38da-6c2b-497a-938b-a34a18c50862" />


## List out the file hello1.txt in the current directory

 __COMMAND AND OUTPUT__

<img width="606" height="172" alt="image" src="https://github.com/user-attachments/assets/136c0c50-ab04-4d9a-8d21-a808e7d3b232" />


## List out all the associated file extensions 

__COMMAND AND OUTPUT__

<img width="717" height="906" alt="image" src="https://github.com/user-attachments/assets/8e296f29-49fd-4a91-ad4a-2ec30998e9cb" />

<img width="886" height="137" alt="image" src="https://github.com/user-attachments/assets/e96d73b9-1f74-4406-b69e-1615ce35b98a" />

<img width="861" height="1087" alt="image" src="https://github.com/user-attachments/assets/89456613-26bf-4736-afab-515f89a6b2b1" />

<img width="912" height="1086" alt="image" src="https://github.com/user-attachments/assets/c4622971-aac8-49dc-b4d2-8b270aae75a3" />

<img width="777" height="1088" alt="image" src="https://github.com/user-attachments/assets/192b4102-8819-44c1-a9aa-e47eacb6f14b" />

<img width="743" height="1089" alt="image" src="https://github.com/user-attachments/assets/9ce22a06-2a9b-404e-99c8-1c5f1fe76278" />

<img width="962" height="1084" alt="image" src="https://github.com/user-attachments/assets/2e581186-79d6-4176-b58d-5857a8a400b6" />

<img width="1028" height="1098" alt="image" src="https://github.com/user-attachments/assets/29e0ca07-4239-412e-8c56-192bfdcfd859" />

<img width="758" height="1087" alt="image" src="https://github.com/user-attachments/assets/21a74474-c217-4a7e-b938-195564104189" />

<img width="790" height="1086" alt="image" src="https://github.com/user-attachments/assets/8e7dcbd7-469a-43b6-b7a4-f8ef48423cad" />

<img width="864" height="1092" alt="image" src="https://github.com/user-attachments/assets/804e8990-9309-4b4d-8ea3-c5a33f4dc89b" />


<img width="1005" height="298" alt="image" src="https://github.com/user-attachments/assets/4a9b6877-054b-4b3a-8d07-7a94ad66e555" />

## Compare the file hello.txt and rose.txt

 __COMMAND AND OUTPUT__

 
<img width="562" height="153" alt="image" src="https://github.com/user-attachments/assets/046c5b3c-d03a-4e69-ab28-14840664082b" />


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

<img width="471" height="131" alt="image" src="https://github.com/user-attachments/assets/ff2559b7-9da7-4874-b86b-39c9a1e6b158" />




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

<img width="688" height="241" alt="image" src="https://github.com/user-attachments/assets/8d309cae-a2ec-4adf-b466-7f3ba51bc69f" />




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

<img width="831" height="261" alt="image" src="https://github.com/user-attachments/assets/7e4f7851-6c6d-408b-921b-6146019f975f" />



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

<img width="599" height="93" alt="image" src="https://github.com/user-attachments/assets/187c2444-092e-4d7a-b4af-98f3c5b4e597" />



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

<img width="411" height="147" alt="image" src="https://github.com/user-attachments/assets/c5a4d09d-c249-47f0-abdc-8a1c6a4ec829" />




<img width="742" height="242" alt="image" src="https://github.com/user-attachments/assets/11578354-4c3a-43cf-a1dd-486f2dc88c87" />




<img width="643" height="171" alt="image" src="https://github.com/user-attachments/assets/c8a99d95-f35a-4863-b172-443cd5bbf9a4" />


# RESULT:
The commands/batch files are executed successfully.

