# Episode 5 : Shortest JS Program, window & this keyword

* The shortest JS program is empty file. Because even then, JS engine does a lot of things. As always, even in this case, it creates the GEC which has memory space and the execution context.

* JS engine creates something known as '**window**'. It is an object, which is created in the global space. It contains lots of functions and variables. These functions and variables can be accessed from anywhere in the program. JS engine also creates a **this** keyword, which points to the **window object** at the global level. So, in summary, along with GEC, a global object (window) and a this variable are created.

* The global object in case of browsers is known as window. Js runs not only in browsers, but in nodejs servers and lot of other devices(like mobile apps). Whereer JS is running there must be a js engine there. In chrome js engine is v8,firefox, iedge have their own js engine. All js engines have responsibility to create global object.In case of browsers it is known as window. Even if our code file is empty then also js engine will create global object.

  ![image](https://github.com/Rahul-0108/namaste-javascript-notes/assets/53996840/c2cf18cd-dead-41f5-875b-8b1055884934)


* In different engines, the name of global object changes. Window in browsers, but in nodeJS it is called something else. At global level, this === window.

* Whenever an execution context(global or functional) is created, a this variable is created with it.

* If we create any variable in the global scope, then the variables get attached to the global object.

eg:
```js
var x = 10;
console.log(x); // 10
console.log(this.x); // 10
console.log(window.x); // 10
```

<hr>

Watch Live On Youtube below:

<a href="https://www.youtube.com/watch?v=QCRpVw2KXf8&ab_channel=AkshaySaini" target="_blank"><img src="https://img.youtube.com/vi/QCRpVw2KXf8/0.jpg" width="750"
alt="Shortest JS Program, window & this keyword Youtube Link"/></a>
