# Programming 101

This is a markdown targetted at providing an overview of the current programming situation. Noticeably, as the field of knowledge regarding programming is too big, this programming 101 might not be able to cover all aspects, but the aspects that are interested to me particularly.

Thank you for your time and attention.

## Keywords Interpretations

|keywords|meaning and definition|
|---|---|
|Object-oriented Language v.s. Procedural/Functional Language||
|Intepreted Language v.s. Compiled Language|According to [Brain's answer](https://stackoverflow.com/a/749218/14499516) in StackOverflow, the boundaries between the two types are actually vague in modern times, especially considering `Java` and `Python`, which the latter one are considered to be an `Interpreted Language` and can runs quicker than `Java`. The idea is to divide the term into five levels:<br>1. Pure interpretation - read a line of source and immediately do what it says (such as `Shell Scripts`).<br>2. Tokenisation+Interpretation - a trivial optimisation that first tokenized each line into streams of tokens to avoid repeatedly performing the same state of interpretation (such as `Basic`).<br>3. Bytecode compilation - transform the code into instructions for a `Virtual Machine (VM)`, and interpret the instructions (such as `Java`, `Python` and `C#`).<br>4. Bytecode+Just-in-Time Interpretation - same as above but to compile the bytecode at the point of execution, allowing runtime analysis and special features utilization on the current processor (such as `later stage Java`, `later stage C#` and `Psyco for Python`).<br>5. Native machine-code compilation - compile directly to the machine code of the target system, but sometimes requires the interpretation to `microcode` if not directly implemented in hardware.|
|Multi-thread Language| |

## Difference between different programming language

The choices of programming languages are picked using the 15 most used programming languages from the two most popular list by [PYPL ranking Septermber 2022](https://pypl.github.io/PYPL.html) and [Stack Overflow's Developer Survey 2022](https://survey.stackoverflow.co/2022/#technology-most-popular-technologies).

The types of programming languages are classified into `Scriping/Interpreted Language`, `High/Middle Level Language`, `Assembly Language`, `Machine Language` and `Binary Code`. The high level is regarded as `Object-oriented` and the middle level is regarded as `Procedural` (also called `functional` in some cases).

|language|type|description(what's special)| applications|
|---|---|---|---|
|Python|High/Middle Level Language|1. Extensive libraries available for import.<br>2. `Write Once Run Anywhere(WORA)` - can be extended and embedded in any languages and platforms,<br>3. **Interpreted language (Dynamic)** - statements are executed one by one, instead of being compiled as a whole (slow execution as a result).<br>4. Simplified Codes and Formatting over `Java` (also no variable types, resulting in a very high memory consumption).|Pros: Web Development, Web Scrapping, AI/Machine Learning, Data Analysis/Visualization, Automated Operation, Financial Analysis<br>Cons: Mobile Development|
|Java|High/Middle Level Language|1. Multi-thread environment - convert bigger task into various threads which run seperately (no need to provide memory to every thread).<br>2. **`Write Once Run Anywhere(WORA)`** - can be converted into byte code (platform-independent) at the compile time with `Java Virtual Machine (JVM)` (as long as the platform has `Java` installed).<br>3. Intepreted language (but also compiled into byte codes) - interpreted during runtime through `JVM` (can run on every operating system, but slower). <br>4. Simplified Codes and Formatting based on `C++` - automatic garbage collection, removed features such as explicit pointers (secured, but cannot access the memory (and other machine interactions) directly), operator overloading, etc.|Pros: Mobile Development, Web-based Applications, GUI Application, Big Data, Distributed Application, Cloud-Based Appliations, IoT Application|
|JavaScript|Scripting/Interpreted Language|1. Interoperability - seamlessly intergrate with other programming languages.<br>2. Client-side language - the client's browser handles `ASCII` text file processing rather than an online server (perform self data validation so the website does not need to be reloaeded entirely; reduce bandwidth usage and decrease wait time for server connections; lower security though).
|C#
|C/C++
|PHP
|R
|TypeScript
|Swift
|Objective-C
|Go
|Rust
|Kotlin
|Matlab
|Ruby
|SQL
|Bash/Shell
|PowerShell

## Difference between different Web Scrapping Libraries in Python

[To be continued]