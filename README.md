# csci3753-assignment-1---part-b-solved
**TO GET THIS SOLUTION VISIT:** [CSCI3753 Assignment 1 – Part B Solved](https://www.ankitcodinghub.com/product/csci3753-pa1-part-b-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;118650&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;2&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (2 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CSCI3753 Assignment 1 - Part B Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (2 votes)    </div>
    </div>
Programming Assignment One – Part B

Writing a second system call

Assuming you’ve gotten hello_world() to work from Part A, you now have to write a second system call. This system call will be given two numbers and an address of where to store the result.

Name this new system call cs3753_add() and define three arguments: number1, number2, and the pointer to result.

As with hello_world, you will need to write a C test program that calls this new system call and passes the correct types of arguments.

Your cs3753_add() must do the following:

use printk() to log the numbers to be added add those two numbers store the result use printk() to log the result return an appropriate return value

Additionally, have your user space test program print out it’s result as well.

Simple Loadable Kernel Module

As we saw in the previous parts, if you make a change to the kernel, you must recompile and then reboot before these changes become active. This approach is time-consuming and can be painstaking. In contrast, LKMs add functionality to the OS without the need to reboot or recompile the entire kernel. In short, LKMs are object files that can be used to extend a running kernel’s functionality on the fly.

LKM Example

Create a directory, /home/kernel/modules, and edit a new file named helloModule.c . Populate this file with the following code:

Notice a few things about the above:

&lt;linux/init. h&gt; &amp; &lt;linux/module.h&gt; contain the library headers for module initialization and other functions that support LKMs

module_init() and module_exit() bind two functions, hello_init() and hello_exit() , to be executed when the module is installed and uninstalled

As with PA1, you cannot use user space functions such as printf() , use printk( ) with KERN_ALERT to write messages to /var/log/syslog

We’ll now use a makefile to build the module. Create a file named Makefile in /home/kernel/modules and add the following line to it:

In this line, obj-m means module, and the line as a whole tells the compiler to create a module object named helloModule.o

To compile the module enter the following command:

and if the compilation is successful, your output should be something similar to:

You can now list out the contents of the /home/kernel/modules directory with the ls -l command:

user@csci3753-vm:/home/kernel/modules$ ls -l

total 276

-rw-rw-r– 1 user user 331 Sep 12 13:04 helloModule.c

-rw-rw-r– 1 user user 127232 Sep 12 13:51 helloModule.ko

-rw-rw-r– 1 user user 603 Sep 12 13:51 helloModule.mod.c

-rw-rw-r– 1 user user 72584 Sep 12 13:51 helloModule.mod.o

-rw-rw-r– 1 user user 57864 Sep 12 13:51 helloModule.o

-rw-rw-r– 1 user user 21 Sep 12 12:56 Makefile

-rw-rw-r– 1 user user 43 Sep 12 13:51 modules.order

-rw-rw-r– 1 user user 0 Sep 12 13:51 Module.symvers

Notice the file named helloModule.ko . This is the kernel module (.ko) object you will be inserting into the running kernel.

Install the module by executing sudo insmod helloModule.ko. Now when you use lsmod, you should see that your module is installed:

Run dmesg or sudo tail /var/log/syslog to see the message emitted by your kernel module when it initialized:

Now remove the module by typing sudo rmmod helloModule . If you again enter the lsmod command, you will see that your module is no longer listed. Type dmesg to see if the expected output from unloading the module is printed:

If the all the above checks out, you’ve successfully completed the first and most basic part of the assignment. Now we can move onto the next part, where you will write a user space test program.

Submission

./arch/x86/kernel/cs3753_add.c

We’ll confirm the operation of your LKM and system call by looking at your Cloud VM.
