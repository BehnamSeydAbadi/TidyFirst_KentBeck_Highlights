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

<p align="justify">
    7. Move Declaration and Initialization Together: Look at the order of the variables declaration, intialization and usage of them. The order of these 3 steps should be in a harmony that keeps the cohesion of the code and logic that helps the developer which reads the code.
</p>

<p align="justify">
    8. 
</p>

<p align="justify">
    9. 
</p>

<p align="justify">
    10. Explicit Parameters: Make input parameters of methods explicit. For example dont use hashmap or anonymous object that holds the required data implicitly. 
</p>

<p align="justify">
    11. Chunk Statements: You’re reading a big chunk of code and you realize, “Oh, this part does this and then that part does that.” Put a blank line between the parts.
</p>

<p align="justify">
    12. Extract Helper: If there is chunk of code which has very limited intraction with the rest of the code, you can make it an extension method or in another language a helper method. There is another scenario, when there are some methods which they always have to be executed in a special and constant order, then make a helper method and call those methods in it's body.
</p>

<p align="justify">
    13. One Pile: Sometimes people break a method or class to very tiny chunks of code that makes the code harder to read. In these times you have to put tiny parts in one place which are relate to each other to make the code readable.
</p>
