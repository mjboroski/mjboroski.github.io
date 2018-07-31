---
layout: post
title:      "JS Variable Declarations"
date:       2018-07-31 22:00:54 +0000
permalink:  js_variable_declarations
---


There are 3 ways to declare variables in Javascript: *var*, *let*, and *const*. I intend to discuss the differences between them, but first we need some background information. We need to talk about *hoisting* and *scope*. 

Understanding *hoisting* is a matter of understanding the order of operations in Javascript. When Javascript runs, it first precompiles, which affects some parts of your code, but not others. What it does on that first pass is, basically, assigns memory. Anything it needs to know exists in order to run properly gets assigned a place in memory. However, it doesn't assign values to these variables and functions until the second pass, or execution of the code. As you could imagine, this leads to problems if you haven't paid attention to the order you've fed the information into the computer through Javascript. 

Javascript treats *var* as though it's assigned at the top of the *scope*. It *hoists* it. This means the variable would be available before it is declared, but it's assignment stays in place. Weird, right? It's important to understand the difference between this behavior and the behaviors of *let* and *const*, which don't get *hoisted*. On the other hand, *const* cannot have its value reassigned once initially assigned. Every *const* declaration must be initialized when it is declared. If *const* is assigned a hash, however, the properties of that hash can be changed.
