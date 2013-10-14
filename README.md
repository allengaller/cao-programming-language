Cao
===

The Cao Programming Language.

Based on Python interpreter.   
   
操语言
=====
   
汲取各种Python, PHP, Ruby精华, 同时避开它们的不足.  这不仅仅是抄袭.
Cao代码清晰易读, 使用范围广泛:   
既能用于OS Kernel, 又能写各种脚本, 还能写大型GUI程序, 可以编译和运行在几乎所有系统上.

Example 范例
=======
The Hello World program: hello.cao

    FUNC Main() int
        IO.p("Hello World!")
        CAO 0
    END
    
Larger example:   
    * Simple HTTP server.
    * STL output.
    
Install and run Cao 安装与运行
===================
Download a clone on this Github project page.
For instructions see the **Getting Started** page.

Discuss Cao 讨论
===============
The maillist is here: 

Why Cao? 为毛操?
===============
Suppose you want to write a new program, something like a text editor. 
What language would you write it in?

    * It has to be as fast as possible, so interpreted languages are out.
    * You don't want to micro manage memory, so C is out.
    * You don't want to require programmers to have a degree, so C++ is out.
    * You want fast startup and not depend on a big runtime, so Java is out.
    * It has to run on most systems, anything with a C compiler, so D is out.
    * You want to have fun making something new.

No existing language really meets these demands, so let's create a new one that does!

Cao is an experimental programming language.  
It is a very practical, no-nonsense kind of language.  
It mixes the good things of many existing languages and avoids their deficiencies.  
And then throws in a few brand new ideas.   

Goals 目标
=========
More on the **Goals** page.

    * easy to read back - code is read N times more often than it is written
    * avoid common mistakes - make it difficult to write bad code (but you can write hacks if you really want to)
    * keep it short and clear, don't state the same thing twice - no header files, don't repeat type specs
    * the effect of a statement should be predictable and not depend on something in another file
    * efficient execution: no startup delay, reasonable memory use - no Just In Time compiler effects, minimize "stop the world" garbage collection.
    * support a wide range of applications - Zimbu can be used to write an OS kernel, a short script and a big GUI application
    * portable - be able to compile and run on almost any system
    * many standard data types, modules and classes - most things you need are already there
    
Choices
=======
    * convert the program to C and use the C compiler to produce machine code (could be something else later)
    * mostly use static type checking, also allow runtime type checking
    * object oriented, all data is handled like an object, but there also are simple types
    * an import defines one symbol, this avoids name conflicts in large projects
    * the standard modules and classes are available without imports, avoids boring work
    * many modules are part of the language, they work the same way everywhere
    * all keywords are in capitals, you can use all other names without worrying about the next version breaking your program