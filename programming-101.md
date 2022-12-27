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

### Major Ones

|language|type|description(what's special)| applications|
|---|---|---|---|
|Python|High/Middle Level Language|1. Extensive libraries available for import.<br>2. `Write Once Run Anywhere(WORA)` - can be extended and embedded in any languages and platforms,<br>3. **Interpreted language (Dynamic)** - statements are executed one by one, instead of being compiled as a whole (slow execution as a result).<br>4. Simplified Codes and Formatting over `Java` (also no variable types, resulting in a very high memory consumption).|Pros: Web Development, Web Scrapping, AI/Machine Learning, Data Analysis/Visualization, Automated Operation, Financial Analysis<br>Cons: Mobile Development<br>Popular libraries: `JUnit`, `Apache Commons`, `Google Guava`, `Mickito Core`.|
|Java|High/Middle Level Language|1. Multi-thread environment - convert bigger task into various threads which run seperately (no need to provide memory to every thread).<br>2. **`Write Once Run Anywhere(WORA)`** - can be converted into byte code (platform-independent) at the compile time with `Java Virtual Machine (JVM)` (as long as the platform has `Java` installed).<br>3. Intepreted language (but also compiled into byte codes) - interpreted during runtime through `JVM` (can run on every operating system, but slower). <br>4. Simplified Codes and Formatting based on `C++` - automatic garbage collection, removed features such as explicit pointers (secured, but cannot access the memory (and other machine interactions) directly), operator overloading, etc.|Pros: Mobile Development, Web-based Applications, GUI Application, Big Data, Distributed Application, Cloud-Based Appliations, IoT Application<br>Pupular libraries: `TensorFlow`, `Numpy`, `PyTorch`, `Pandas`.|
|JavaScript|Scripting/Interpreted Language|1. Interoperability - seamlessly intergrate with other programming languages.<br>2. Client-side language - the client's browser handles `ASCII` text file processing rather than an online server.<br>- perform self data validation so the website does not need to be reloaeded entirely.<br>- reduce bandwidth usage and decrease wait time for server connections.<br>- lower security though.<br>- strict requirements on browser supports (affects interpretation).<br>- difficult for debugging - ignored instead of displayed errors.<br>3. Only support single `inheritance`.|Pros: Web-based Applications (Interactive), Mobile Development, Server-side Development (Simple)<br>Popular libraries: `jQuery`, `React`, `D3.js`, `Underscore.js`.|
|C#|High/Middle Level Language|1. A part of `.NET Framework` - support different runtime environment such as `aforementioned Mono` and `Microsoft's CLI` (provides interoperability; high dependency compared to `Java` as it requires `Window hosting` and `.NET Framework` is not all backward compatible).<br>2. `Static typing` - check `type` at compile time (with `type safety` ensured - unchangable types for variables.<br>3. Interpreted language (but also compiled into `intermediate language (IL)` - interpreted during runtime with `common language runtime (CLR)`.<br>4. Simplified Codes and Formatting based on `C` (provide limited memory access and pointer features; in-built garbage collector tho).|Pros: OS Applications, Web-based Applications, Mobile Development<br>Popular libraries: N/A|
|C++|High/Middle Level Language|1. Combined features of `C` and `Simula 67` - preserve `C` features such as pointer and memory management; yet still object-oriented; yet absence with garbage collector or built-in threads.<br>|Pros: System Programming, GUI-based Applications, Browsers Development, Database Management Software, Finance Applications, Cloud/Distributed Systems|
|C|Middle Level Language|1. Simple and Highly Portable - based on `ASCII` characters and is compatible with wide range of operating systems and platforms; only 32 keywords with large number of built-in functions.<br>2. `System-programming` - allow communication with hardware (such as memory alloation, pointer).<br>3. Oldest yet still in use (large amount) - lack of exception handling, run-time checking or strict type checking, constructor or inheritance, etc.|Pros: System Programming, GUI-based Applications, Database Management Software (such as `MySQL`), Langugage Programming.<br>Popular libraries: N/A|

### Minor Ones

Other popular languages: |PHP
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

|libraries|type|description|
|---|---|---|
|*Interacting with webpages*||
|Requests|HTTP library|A simple API for interacting with `HTTP` operations such as `GET`, `POST`, etc.<br>1. Can send request to the HTTP server, and `GET` response back in the form of `HTML` or `JSON` response. <br>2. Can send `POST` requests to modify or add some content.|
|Urllib3|HTTP library|A user-friendly and standard `HTTP` client that collects several modules working with `URLs`.<br><br>Even `requests` library internally uses `urllib3`.|
|*Parsing broken `HTML`*||
|BeautifulSoup|Python library|A Python library that are designed to extract data from `HTML` and `XML` files, yet requiring the help of `HTML` libraries and parsers.<br><br>`beautiful soups` now support internal `lxml parsing`.<br><br>Here's some advantages and disadvantages of the internal parsers (extracted from the [official website](https://www.crummy.com/software/BeautifulSoup/bs4/doc/#installing-a-parser)):<br><table><tr><th>Name</th><th>Advantages</th><th>disadvantages</th></tr><tr><td>Python's html.parser</td><td>1. Batteries included<br>2. Decent speed<br>3. Lenient (as of `Python` 3.2. and after)</td><td>1. Not very lenient compared to `html5lib`<br>2. Slower than `lxml`</td></tr><tr><td>lxml's `HTML `parser</td><td>1. Very fast<br>2. Lenient</td><td>1. External `C` dependency</td></tr><tr><td>lxml's `XML` parser</td><td>1. Very fast<br>2. The only currently supported `XML` parser</td><td>1. External `C` dependency</td></tr><tr><td>html5lib</td><td>1. Extremely lenient<br>2. Parses pages as same as a web browser does<br>3. Creates valid `HTML5`</td><td>1. Very slow<br>2. External `Python` dependency</td></tr></table><br>Simple for beginners and suitable for a few particular websites that requires crawling.|
|lxml|Python library|A `Python` library that handles `XML` and `HTML` files easily.<br><br>As mentioned by [simon](https://stackoverflow.com/a/4967121/14499516), it performs better when the source is well-formed, yet it is very fast.|
|*Processing the whole web scrapping procedures (able)*||
|Scrapy|Web Crawling Framework|A high-level web-crawling framework that are designed to scrape large scale of websites.<br><br>Suitable for websites with `JavaScript` or `AJAX` dynamic data loading technologies, or login authentication and search mechanism.|
|Selenium|Automation Testing Tool|An open-source automation testing tool taht control web browsers through programs and perform browser automation.<br><br>Suitable for large-scale web cralwer projects, which have certain efficiency requirements and need to deal with complex crawling logic.|


