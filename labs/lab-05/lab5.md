# Lab5 - Build Systems
## Step 1
### tutorial.cxx
[Step1: tutorial.cxx](https://github.com/Dani926/oss-repo/blob/master/labs/lab-05/Step1/tutorial.cxx)
### CMakeLists
[Step1: CMakeLists.txt](https://github.com/Dani926/oss-repo/blob/master/labs/lab-05/Step1/CMakeLists.txt)
### Tutorial Output
![Step1](https://user-images.githubusercontent.com/63828111/109912234-a5d4b600-7c79-11eb-846e-6a9902f84790.png)
## Step 2
### tutorial.cxx
[Step2: tutorial.cxx](https://github.com/Dani926/oss-repo/blob/master/labs/lab-05/Step2/tutorial.cxx)
### CMakeLists
[Step2: CMakeLists.txt](https://github.com/Dani926/oss-repo/blob/master/labs/lab-05/Step2/CMakeLists.txt)
### Tutorial Output
![Step2](https://user-images.githubusercontent.com/63828111/109912235-a5d4b600-7c79-11eb-9d37-cd3b3b9a4fb6.png)
## Step 3
### CMakeLists
[Step3: CMakeLists.txt](https://github.com/Dani926/oss-repo/blob/master/labs/lab-05/Step3/CMakeLists.txt)
### MathFunctions/CMakeLists
[Step3: MathFunctions/CMakeLists.txt](https://github.com/Dani926/oss-repo/blob/master/labs/lab-05/Step3/CMakeLists%20-%20MathFunctions.txt)
### Tutorial Output
![Step3](https://user-images.githubusercontent.com/63828111/109912238-a66d4c80-7c79-11eb-9ded-84d1483bf991.png)
## Step 4
### CMakeLists
[Step4: CMakeLists.txt](https://github.com/Dani926/oss-repo/blob/master/labs/lab-05/Step4/CMakeLists.txt)
### MathFunctions/CMakeLists
[Step4: MathFunctions/CMakeLists.txt](https://github.com/Dani926/oss-repo/blob/master/labs/lab-05/Step4/CMakeLists%20-%20MathFunctions.txt)
### ctest -VV Output
![Step4](https://user-images.githubusercontent.com/63828111/109912239-a66d4c80-7c79-11eb-92c9-127e08434c19.png)
## Step 5
### CMakeLists
[Step5: CMakeLists.txt](https://github.com/Dani926/oss-repo/blob/master/labs/lab-05/Step5/CMakeLists.txt)
### MathFunctions/CMakeLists
[Step5: MathFunctions/CMakeLists.txt](https://github.com/Dani926/oss-repo/blob/master/labs/lab-05/Step5/CMakeLists.txt)
### Tutorial Output
![Step5](https://user-images.githubusercontent.com/63828111/109912241-a66d4c80-7c79-11eb-8453-ffc846492afc.png)

## BuildSystemsExample
### Makefile
```
static_block: program.c libblock.a
	gcc program.c -L. -lblock -o static_block

dynamic_block: program.c libblock.so
	gcc program.c -L. -l:libblock.so -o dynamic_block

libblock.a: s_block.o
	ar -rc libblock.a s_block.o

libblock.so: d_block.o
	gcc -shared d_block.o -o libblock.so

s_block.o: source/block.c
	gcc -c source/block.c -o s_block.o

d_block.o: source/block.c
	gcc -c -fpic source/block.c -o d_block.o

clean:
	$(RM) static_block dynamic_block libblock.a libblock.so *.o
```
  
## Makefile Static Block Output
![StMakeStatic](https://user-images.githubusercontent.com/63828111/109912243-a705e300-7c79-11eb-9fbc-733cf83e0eb9.png)
## Makefile Dynamic Block Output
![StMakeDynamic](https://user-images.githubusercontent.com/63828111/109912242-a705e300-7c79-11eb-9115-89377f55b975.png)
## CMakeLists.txt

## CMakeLists.txt Makefile

## CMakeLists.txt Static Block Output
![StCmakeStatic](https://user-images.githubusercontent.com/63828111/109912233-a5d4b600-7c79-11eb-96a1-519238244a8d.png)
## CMakeLists.txt Dynamic Block Output
![StCmakeDynamic](https://user-images.githubusercontent.com/63828111/109912232-a5d4b600-7c79-11eb-89f1-c5fa24291b0d.png)
## Static VS Dynamic Sizes
![StaticVsDynamic](https://user-images.githubusercontent.com/63828111/109912231-a53c1f80-7c79-11eb-8185-ab4c30b0a38c.png)









