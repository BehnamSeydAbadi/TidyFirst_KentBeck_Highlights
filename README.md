# TidyFirst_KentBeck_Highlights
Here is my Highlights of Tidy First? book. It has been written by Kent Beck.

<p align="center">
    <img src="./Tidy%20First%20-%20Kent%20Beck%20-%20Highlights.png" />
</p>

<h4>
  Part I: Tidyingg  
</h4>

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
    8. Explaining Variables: Break big expressions to multiple small expressions and keep them in variables with meaningfull names.
</p>

<p align="center">
    ATTENTION: As always, separate the tidying commit from the behavior change commit.
</p>

<p align="justify">
    9. Explaining Constants: Make hard coded numbers and strings and ..., into a constant variable with meaningfull name. Remember before using one constant variable instead of a repeated hardcode value, check the meaning of that value in the context of the code. Because it's meaning can be something totaly different than the constant variable which it's value is equal to the mentioned one.
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

<p align="justify">
    14. Explaining Comments: When reading a code, and you get to "Hah, now I get it" point, write down what things made the code complicated. When you don't want to change the code, or you don't have time to do it, try to write some meaningful comments for the complicated parts. Write the comments in a way that other readers in future can figure it out with no difficulty.
</p>

<p align="justify">
    15. Delete Redundant Comments: If there is a simple and straightforward code, and it has some comments to explain it, then just delete it. Writing comment for any code is a bad thing. Because it consumes the reader's time.
</p>


<h4>
  Part II: Managing  
</h4>

<p align="justify">
    16. Separate Tidying: There some pull requests which the behavior changes and tydings are included. These kind of pull requests get too large that makes it hard for reviewers to read and understand the changes. When pull requests get separated based on behavior changes and tydings, the count of pull requests increases. But after a few pull requests a pattern comes with the order of pull requests. There are some pros and cons that need trade-offs to choose a suitable pull request for the team.
</p>

<p align="justify">
    17. Chaining: In tidying, you should be aware of how much tidying is too much tidying. Because tidying is like potato chips. When you do one tidying, you want more. Remember, when tidyings get too much and too fast, it's a smell that you are over tidying that can become a failed tidying.
</p>

<p align="justify">
    18. Batch Sizes: In tidying, you should remember that you are making things right to make the playground ready for the requested behavior changes. To get the balance in trade-offs of tidying you need to checkout these three parts:
I) Collisions: The more tidyings per batch, the longer the delay before integrating, and the greater the chance that a tidying collides with work someone else is doing.
II) Interactions: the chance of a batch accidentally changing behavior rises with the number of tidyings in the batch.
III) Speculation: The more tidyings per batch, the more we are prone to tidying just because, with all the additional costs that creates
</p>

<p align="justify">
    19. Rhythm: The reason of tidying is to make behavior changes easy in future. The tidying should take a few minutes to one hour. If it passes one hour you neen to be carefull. Because it could be you are going in a wrong path. To figure out you should check it out and think again what's going on. If it was reasnable for you to do tidying more than one hour then you should keep on. But it should not take more than that, if it happen check it again.
</p>

<p align="justify">
    20. Getting Untangled: You pass a test, then you tidy the code. You pass another test, then you tidy the code again. This cycle keeps on and on. Once you see that there is a mess in your commits and pull requests. Because it's messy and for reviewers of the pull request it's hard to figure it out what's going on. The best option is to undo every thing do it all again to keep the commits and pull requests clean and make it easer for reviewers to read it.
</p>

<p>21. First, After, Later, Never:</p>
<p>Avoid tidying when:</p> <ul> <li>You will no longer make changes to this code.</li> <li>There is no educational value in enhancing the design.</li> </ul> <p>Tidy at a later time when:</p> <ul> <li>You have a substantial amount of tidying to do without any immediate benefits.</li> <li>There will eventually be a reward for completing the tidying.</li> <li>You can tidy in smaller increments.</li> </ul> <p>Tidy afterwards when:</p> <ul> <li>Postponing tidying until the next opportunity will incur higher costs.</li> <li>You will not experience a sense of accomplishment if you don't tidy afterwards.</li> </ul> <p>Tidy as a priority when:</p> <ul> <li>It will yield immediate benefits, either through enhanced comprehension or cost reduction.</li> <li>You are aware of what needs to be tidied and how.</li> </ul>
