Programmer: Ali Raza Roll no: K21-4703 
Step 01: First we need to download these modules: • sudo apt-get install gcc • sudo apt-get install libncurses5-dev • sudo apt-get install bison • sudo apt-get install flex • sudo apt install make • sudo apt-get install libssl-dev • sudo apt-get install libelf-dev • sudo add-apt-repository "deb http://archive.ubuntu.com/ubuntu $(lsb_release -sc) main universe" • sudo apt-get update • sudo apt-get upgrade  
![image](https://user-images.githubusercontent.com/107793398/221270833-8be61201-672a-4954-b2da-701820d5b707.png)

 
Step 02: Making a new folder called hello:
Step 03: Adding a C code for the system call (hello.c file is mentioned/uploaded above)
Step 04: Creating a Makefile for the C code ( Makefile is mentioned/uploaded above)
 
Step 05: Adding the new code into the system table file:
 
Step 06: Adding the prototype of the new system call into the system calls header file:
 ![image](https://user-images.githubusercontent.com/107793398/221266682-44f4d329-1f4e-470f-80a2-ddb7f9b8012f.png)

Step 07: Changing version and adding the hello folder in the kernel’s Makefile, change  EXTRAVERSION to my roll number:
 ![image](https://user-images.githubusercontent.com/107793398/221266746-4f0ae338-3392-4c52-8618-50de2e3b1827.png)

Step 08: Creating a config file:
 
 
 
Step 09: Cleaning and Compiling the kernel: . 





Step 10: Installing modules for the kernel:
 ![image](https://user-images.githubusercontent.com/107793398/221266907-287cc49d-b9bf-40af-a01f-33d575737e24.png)














Here done is showing modules are installed successfully:
 











Step 11: Checking if the System call is Working Properly: 
After logging into the newly compiled kernel, we check the system call by making a C code named “userspace.c” and putting the following code in it:
This userspace.c file is mentioned/uploaded above.
 
“uname -r” is showing that our new kernel is build and running successfully for further checking, executing userspace.c file by making an object and typing “./a.out”. If it returns 0, this means that our code has compiled successfully and the system call is working fine (Note that in calling syscall(335), 335 is the number where we added our system call in the table)
 
Finally, I run "dmesg" to view the kernel messages, and we will find "Hello World" written at the end of them. If it returns 0, this means that our code has successfully compiled, and the system call is functioning properly.
 

 
OS Assignment 1/ ALI RAZA/ 21K-4703/ BAI-AI
