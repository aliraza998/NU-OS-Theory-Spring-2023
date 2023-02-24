Programmer: Ali Raza Roll no: K21-4703 


Step 01: First we need to download these modules: • sudo apt-get install gcc • sudo apt-get install libncurses5-dev • sudo apt-get install bison • sudo apt-get install flex • sudo apt install make • sudo apt-get install libssl-dev • sudo apt-get install libelf-dev • sudo add-apt-repository "deb http://archive.ubuntu.com/ubuntu $(lsb_release -sc) main universe" • sudo apt-get update • sudo apt-get upgrade  
![image](https://user-images.githubusercontent.com/107793398/221270833-8be61201-672a-4954-b2da-701820d5b707.png)
![image](https://user-images.githubusercontent.com/107793398/221272776-d7851981-a3b9-4d40-b0cb-2442cc922fa9.png)
 
Step 02: Making a new folder called hello:

Step 03: Adding a C code for the system call (hello.c file is mentioned/uploaded above)

Step 04: Creating a Makefile for the C code ( Makefile is mentioned/uploaded above)
![image](https://user-images.githubusercontent.com/107793398/221272835-4e57f959-1a55-48f9-9c75-2029da6ded06.png)

Step 05: Adding the new code into the system table file:
![image](https://user-images.githubusercontent.com/107793398/221273708-c877b3cb-95c5-47e1-9399-c958b2eccdcf.png)

Step 06: Adding the prototype of the new system call into the system calls header file:
![image](https://user-images.githubusercontent.com/107793398/221273809-1266442b-0cb0-419c-a132-adc5c526300d.png)

Step 07: Changing version and adding the hello folder in the kernel’s Makefile, change  EXTRAVERSION to my roll number:
![image](https://user-images.githubusercontent.com/107793398/221271933-2ff2fb41-2b26-458f-bf21-5db052a5d90c.png)


Step 08: Creating a config file:
![image](https://user-images.githubusercontent.com/107793398/221276650-55fb7f72-1791-479d-a5be-ed5bf856edf8.png)
![image](https://user-images.githubusercontent.com/107793398/221273051-be3aab66-bb3b-4b55-9b47-9441400628e1.png)
![image](https://user-images.githubusercontent.com/107793398/221273080-06c51a6a-de6b-4fde-b422-19454c70e32d.png)
![image](https://user-images.githubusercontent.com/107793398/221273098-3a2f284d-e97c-4cc8-8792-fdcef7989afa.png)

Step 09: Cleaning and Compiling the kernel: . 
![image](https://user-images.githubusercontent.com/107793398/221273147-2e3d0df4-720e-441e-951d-11010f22b44b.png)
![image](https://user-images.githubusercontent.com/107793398/221273178-efc0755c-a9d5-42d5-b802-1b0704f8a4eb.png)

Step 10: Installing modules for the kernel:
![image](https://user-images.githubusercontent.com/107793398/221274103-909dc3d3-1867-461e-a70b-f302183578a0.png)

Here done is showing modules are installed successfully:
 ![image](https://user-images.githubusercontent.com/107793398/221273252-67a8f28d-ff32-4141-8676-216aa8135e13.png)

Step 11: Checking if the System call is Working Properly: 
After logging into the newly compiled kernel, we check the system call by making a C code named “userspace.c” and putting the following code in it:
This userspace.c file is mentioned/uploaded above.
 ![image](https://user-images.githubusercontent.com/107793398/221273286-530e8ce1-59d5-4780-9a1a-4177014c6df2.png)

“uname -r” is showing that our new kernel is build and running successfully for further checking, executing userspace.c file by making an object and typing “./a.out”. If it returns 0, this means that our code has compiled successfully and the system call is working fine (Note that in calling syscall(335), 335 is the number where we added our system call in the table)
 ![image](https://user-images.githubusercontent.com/107793398/221273318-c6471faf-ef9c-4634-8982-90889354cb25.png)

Finally, I run "dmesg" to view the kernel messages, and we will find "Hello World" written at the end of them. If it returns 0, this means that our code has successfully compiled, and the system call is functioning properly.
 ![image](https://user-images.githubusercontent.com/107793398/221273381-36093822-84fc-48cc-b4c3-2ba8e976e70d.png)
![image](https://user-images.githubusercontent.com/107793398/221273409-81c9d6f9-7db1-483e-8f1c-b6cb891e8b0f.png)


 
OS Assignment 1/ ALI RAZA/ 21K-4703/ BAI-AI
