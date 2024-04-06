# TidyFirst_KentBeck_Highlights
Here is my Highlights of Tidy First? book. It has been written by Kent Beck.

<p align="center">
    <img src="./Tidy%20First%20-%20Kent%20Beck%20-%20Highlights.png" />
</p>

<p align="justify">
1. Guard Clauses: Use guard clauses as long as the code does not get complicated. The "Only one return" rule is deprecated and it is for FORTRAN period. It's better to use multiple returns instead of huge gaurd clauses.
</p>

<p align="justify">
2. Dead Code: Just delete it. If the dead code gets needed in future we can get it back from version control.
</p>

<p align="justify">
3. Normalize Symmetries: Follow a specific codding pattern in your application. For example the way you write if statment or loops, just keep writing them in one way dont use different variants of if statement or loop implementations.
</p>

<p align="justify">
4. New Interface, Old Implementation: There is an interface that is messy and you want to use it? It's ok just write another simple interface that suits you well, then make the old implementation pass-through the new interface by using Adapter pattern. Now you are using the old implementation with new clean and short interface.
</p>

<p align="justify">
5. Reading Order: When reading a source code, dont try to change the behaviour or it's core material. Make it more readable by reordering elements of the code (if the code is not sensitive to order of functions or variables).
</p>

<p align="justify">
6. Cohesion Order: Keep classes and functions which are couple to each other close to each other. Try to put files related to each other in the same directory. If there are some couple code and you can afford the decoupling and removing the repeated codes, then do it. To figure it out you can do it or not use this formula: <span> cost(decoupling) + cost(change) < cost(coupling) + cost(change) </span>
Remember, Sometimes better cohesion helps you live with the coupling.
</p>
