# Episode 16 : JS Engine Exposed, Google's V8 Architecture

* JS runs literally everywhere from smart watch to robots to browsers because of Javascript Runtime Environment (JRE).

* JRE is like a big container which has everything which are required to run Javascript code.

* JRE consists of a JS Engine (❤️ of JRE) where our code runs, set of APIs to connect with outside environment, event loop, Callback queue, Microtask queue etc.

* Browser can execute javascript code because it has the Javascript Runtime Environment. Node.js has also JRE.

 ![image](https://github.com/Rahul-0108/namaste-javascript-notes/assets/53996840/19514043-ba44-424a-abc5-d4a2bd9ad773)

* Suppose we want to run js code inside water cooler, we need in it JRE. Inside JRE, we will have JS Engine, API(like getWaterLevel(just like localstorage api of browser) to get watere level from water cooler(superpower) which can be accessed using a global object inside js code).

* Browser and Node.js JREs have implemented their own apis differently though their names can be same like console.log, setTimeout. APIs help to access outer environment of devices.


* ECMAScript is a governing body of JS. It has set of rules which are followed by all JS engines like Chakra(Edge), Spidermonkey(Firefox)(first javascript engine created by JS creator himself), v8(Chrome). We can also create our own Js Engine. We need to make sure We follow all ECMAScript standards.

* Javascript Engine is not a machine. Its software written in low level languages (eg. C++) that takes in hi-level code in JS and spits out low level machine code.

* Code inside Javascript Engine passes through 3 steps : **Parsing**, **Compilation** and **Execution**
    1. **Parsing** - Code is broken down into tokens. In "let a = 7" -> let, a, =, 7 are all tokens. Also we have a syntax parser that takes code and converts it into an AST (Abstract Syntax Tree) which is a JSON with all key values like type, start, end, body etc (looks like package.json but for a line of code in JS. Kinda unimportant)(Check out astexplorer.net -> converts line of code into AST).
    ![image](https://github.com/Rahul-0108/namaste-javascript-notes/assets/53996840/e0fc1154-87fa-46d2-a8a9-aa55bd51f06f)

    3. **Compilation** - In Interpretter programming languages, code is executed without compiling into low level language. The actual code is executed.It does not use compiler to compile code. But in compiling languages, code is compiled into low level language and then executed.  Java is a compiling language.  JS has something called Just-in-time(JIT) Compilation - uses both interpreter & compiler. Both compilation and execution both go hand in hand. The AST from previous step goes to interpreter which converts hi-level code to byte code and moves to execeution. While interpreting, compiler also works hand in hand with interpreter to compile and form optimized code during runtime.There are other optimizations which the compiler does in the code like inlining, copy elision,inline caching. **Does JavaScript really Compiles?** The answer is a loud **YES**. More info at: [Link 1](https://github.com/getify/You-Dont-Know-JS/blob/2nd-ed/get-started/ch1.md#whats-in-an-interpretation), [Link 2](https://web.stanford.edu/class/cs98si/slides/overview.html), [Link 3](https://blog.greenroots.info/javascript-interpreted-or-compiled-the-debate-is-over-ckb092cv302mtl6s17t14hq1j). JS used to be only interpreter in old times, but now has both to compile and interpreter code and this make JS a JIT compiled language, its like best of both world.
    4. **Execution** - Needs 2 components ie. Memory heap(place where all memory is stored, place where all variables and funcs are assigned memory) and Call Stack(same call stack from prev episodes). There is also a garbage collector(tries to free memory space like unused functs and variables). It uses an algo called **Mark and Sweep** for garbage collecting.
    ![JS Engine Demo](/assets/jsengine.jpg)
    GiF Demo
    ![JS Engine Demo](/assets/jsenginegif.gif)

* Companies use different JS engines and each try to make theirs the best and optimized the code most to be as fast as possible. Currently Google's v8 engine is the fastest now.
    * v8 of Google has Interpreter called Ignition, a compiler called Turbo Fan and garbage collector called Orinoco
    * v8 architecture:
    ![JS Engine Demo](/assets/jsengine.png)




<hr>

Watch Live On Youtube below:

<a href="https://www.youtube.com/watch?v=2WJL19wDH68&ab_channel=AkshaySaini" target="_blank"><img src="https://img.youtube.com/vi/2WJL19wDH68/0.jpg" width="750"
alt="JS Engine Exposed, Google's V8 Architecture in JS Youtube Link"/></a>
