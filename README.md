# OS-Workshop
## AIM:
To Modify the Minix Boot Process which includes our name in it.
## STEPS TO MODIFY THE MINIX BOOT PROCESS:
### 1. Set Up Minix Development Environment:
1. Download Minix from [here](http://lms2.cse.saveetha.in/mod/url/view.php?id=718)
2. Set up the Minix development environment by following the instructions provided in the Minix documentation. Refer to this [video](http://lms2.cse.saveetha.in/mod/url/view.php?id=735) for guidance.

### 2. Locate Boot Code:

1. Identify the relevant source code files for the Minix boot process. Common files include boot/boot.asm, boot/boot.h, and /src/kernel/main.c.
### 3. Insert Your Code:
    ```
    ## Announce
    static void announce (void)
    {
        printf("\nMINIX %s %s. "
        #ifdef _VCS_REVISION
            "(" _VCS_REVISION ")\n"
        #endif
            "Copyright 2012, Vrije Universiteit, Amsterdam, The Netherlands\n",OS_RELEASE, OS_VERSION);
        printf("MINIX is open source software, see http://www.minix3.org\n");
        // Add here
        printf("MINIX is Modified by VISHWARAJ G.\n");
    }
    ```
### 4. Compile and Build:
Use the Minix build system to compile your modified code.
```
make build
```
### 5. Reboot:
Reboot Minix to See your modified changes
## OUTPUT:
![alt text](<Screenshot (571).png>)
![alt text](<Screenshot (572).png>)
## RESULT:
Thus the program to modify the MINIX boot process is compiled and executed successfully.