# Chapter 1: Clean Code
We will never be able to get rid of code completely because codes are the languages in which we represent requirements. Being able to state requirements in a way that the machine can understand is programming. So the code will always exist.

When we write code when we have work to do, we can write bad code with the feeling of "I'll fix it later". However, later on, the codes are not edited and eventually it can become inextricable. Be careful!

When it becomes too bad to ensure continuity, it may be necessary to redesign the system. This shows us that writing clean code actually reduces the time cost.

When requirements change, we complain that the code also changes and that just one line of code affects hundreds of modules, and we blame managers and customers. Actually, we are the real culprits here.

Writing messy codes to get things done on time will actually prevent us from getting things done because after a while that mess will slow us down. All we have to do is always keep the code as clean as possible.

Writing clean code is like painting, most of us can distinguish between good and bad image, but just because we can distinguish it doesn't mean we can paint well. So just because we can distinguish clean and dirty code doesn't mean we can write clean code.

Writing clean code requires the disciplined application of lots of little techniques applied with a sense of "cleanliness". This is the "code sense" key. A programmer without a "code sense" would have no idea what to do, even if he realizes that the code is messy. A programmer with a "code sense", on the other hand, will see various ways to optimize it when he sees messy code.

Many definitions and requirements for clean code can be written.

* Clean code is pleasing to read.

* Clean code should be efficient, wasted cycles are inelegant so they are also not pleasing.

* Bad code tempts the mess to grow! When others change bad code, they tend to make it worse.

* Error handing should be complete in clean code.

* Bad code tries to do too much, has mixed intent and ambiguity of purpose. Clean code is focused. Each function, each class, and each module focuses on a single task.

* Clean code should read like well-written prose. 

* Our code should be realistic, not speculative. It should contain only what is necessary. Our readers should perceive us as determined.

* Clean code makes it easy for other people to enhance it

* Code, without tests, is not clean. No matter how elegant it is, no matter how readable and accessible, if it hath not tests, it be unclean.

* Clean code should be small, rather than that is large.

* Code should be composed in such a form as to make it readable by humans.

* Clean code is code that someone takes the time to deal with and make regular fixes and improvements to.

* Clean code has no duplication, one thing, expressiveness, tiny abstractions.

Even if we apply all of these things, it is not enough to write clean code. The code has to be kept clean over time


# Chapter 2: Meaningful Names
We use naming all over the project, so we need the best naming.

Naming needs to be clear to everyone, it needs to tell directly what it's aiming for and why it exists.

We should avoid giving false clues that obscure the meaning of the code. So the same thing should come to life in the minds of everyone who looks at the name.

We should not use words that can only be known by programmers.

Avoid two long names in two different places where there are only minor differences. Because if this small difference is not noticed by the reader, it may cause misunderstanding. Most of us use auto-completion when we write code so it can be very normal to go unnoticed.

This difference must be significant if we want to indicate that they are different when naming two similar variables. We should not try to create this difference by adding just one letter or just one word to the beginning or end of the variables.

Naming need to be pronounced, if when we're arguing with someone about code and can't pronounce the nomenclature, there are things we need to fix.

We should not make the naming in the form of a single character, the naming should be easily searchable in the file. A single letter will make it difficult for us to search, as it can also appear in other nomenclatures. We can only use single letter naming as a local variable in a very short method.

Avoid encodings, because encoded names are seldom pronounceable and are easy to mis-type.

We do not need to use prefix or suffix in naming, because this is ignored by the reader anyway and only the meaningful part of the naming is looked at.

Readers shouldn't have to mentally translate your names into aliases they already know.

Class and object names can be nouns or noun phrases, not a verb.

Method names must have verb or verb phrase names. In addition, methods must be named according to their accessors, mutators, and predicates, and must be prefixed with get,set,is.

When constructors are overloaded, define a method with a naming that describes the argument it will take.

Identify a word for a particular concept and use it everywhere. But we should also avoid using the same word for two different purposes. This will cause confusion for the reader.

We should not forget that the people who will read our codes are programmers, in which case we can use technical terms such as computer science terms and algorithm names in our naming.

Use the name from the problem domain. At least the programmer who maintains your code can ask a domain expert what it means.

We should not add unnecessary-reasonable contexts to the beginning of the nomenclature. Short names are always better than long ones as long as they are meaningful because they are more readable.

# Chapter 3: Functions
In terms of readability of the code, the functions we write should be small.

A function's indentation level should not be greater than one or two, which also means that the function should not be large enough to hold nested structures.

The functions we write should only do one task. If we can divide the codes in a function we wrote into sub-functions in a meaningful way, it means that our function is doing more than one job.

Functions that do one thing cannot be reasonably divided into sections.

Mixing levels of abstraction within a function is always confusing. We need to make sure that the statements within our function are all at the same level of abstraction.

Each function must introduce the next, and each function must remain at a consistent level of abstraction.

Switch statements can be used to create polymorphic objects when they appear only once.

When naming the function, it is necessary to choose a descriptive name. The smaller and more focused the function, the easier it is to choose a descriptive name.

A long descriptive name is better than a short enigmatic name

Be consistent in your names. Use the same phrases, nouns, and verbs in the function names you choose for your modules.

The ideal number of arguments for a function is 0. Then comes 1 and 2, respectively, but we should avoid 3 arguments or more, except in very special cases, and we should never use more than 3 arguments.

The increase in the number of arguments will make the tests we will write more difficult. Because we will have different combinations to try.

If a function is going to convert the input argument, it should appear as the conversion return value. Otherwise, it may be confusing.

It is very wrong to pass a flag value as an argument, because it causes the function to do 2 things when we pass the flag value. One job if true, another job if not.

It is a situation that we will always encounter when a function takes two arguments, we should consider the cost and evaluate the options that we can reduce to one argument.

To reduce the number of variables, we can group related values into objects.

When specifying a function name, choosing a name that specifies the function's purpose, the order of the variables, and their purpose saves us a lot.

If your function needs to change the state of something, have it change the state of the object it owns.

Your function must either do something or respond to something. It shouldn't do two things at the same time.

In cases where functions fail, use exception instead of returning error code, then it will be simpler to handle the error.

Extract the bodies of the try and catch blocks out into functions of their own. We said that functions should only do one thing, error catching is a job. So there shouldn't be anything else where the error catch is. Should be divided into Functions

Duplication may be the root of all evil in software. Many software principles that we know and use have been developed to prevent this.

Writing code is actually like writing anything. It is optimized by first creating a sketch and then making changes to it. Splitting it into sub-functions, making the names neater, reducing duplications.

# Chapter 4: Comments
Well written comments can be very helpful to the reader, while poorly written comments can be very damaging.

Actually, commenting means that we cannot express ourselves with code. Before adding a comment line, reconsider if you can express yourself with code.

The written codes may change over time, if the comment lines are not updated, it will mislead the reader. So the only thing that tells the truth is the code that has been written.

Again, we can say that the best comment is the one where you find a way not to write a comment.

Other than that, in some cases it may be good to use comment lines.

* For example, copyright and authorship statements that we need to add due to the institution we work for can be added to the beginning of each source file.

* We can give simple information about the method with a comment line.

* The purpose behind a decision made in the code can be explained.

* We can translate the meaning of some obscure argument or return value into something that’s readable in comments.

* It can be used to inform other people working on the project about something.

* Reminders can be left with a comment line for things to do later.

* It can be used to emphasize that a place is really very important.

Apart from this, in some cases it is wrong to use a comment line.

* It is wrong to comment just because we feel compelled to comment. Every comment we have to look at another module to understand the comment is misspelled.

* In cases where we give wrong information, using a comment line should never be done because it will mislead the reader.

* The rule that every function must have a comment line is absolutely wrong and complicates the code.

* One thing that is very obvious should not be commented out.

* We should not explain something that we can describe with a variable or function in the comment line, we should explain it with code.

* In long code, programmers can use comments to indicate who owns the curly brace. Shorten the code instead.

* We should not comment out old codes, we should delete them directly.

* Using HTML in comment lines makes it very difficult to read, we shouldn't.

* Make sure your comment describes the code it appears next to. Do not provide system-wide information in a local comment.

* Have a clear and precise link between the comment and the code. An interpretation that the reader cannot understand is useless.

* Short and well-named functions will often not need any comment headers.

#Chapter 5: Formatting
In order for people reading the code to be able to read it comfortably, it must be well formatted. If we are working individually, we must determine and apply our own rules; if we are working with a team, we must determine and apply certain formats that everyone in the team will follow.

Let's think about article writing, there will be a title at the top and it gives us an idea about the article. Afterwards, the events are mentioned in the first paragraph without going into details, and we learn these details as we continue to read. Code writing should be like this, naming should give an idea about the code. The top of the code should give information about the algorithms and the details should be learned as you go to the lower functions.

If there is a different concept in a part of the code, we can make it more readable by separating it with vertical space. For example, after imports, after variable declarations are finished, or after each function declaration.

Related concepts should be kept close to each other vertically, otherwise it may be difficult to search within the file.

* It is necessary to define variables close to where they are used. Also, control variables defined for the loop must be defined inside the loop.

* Instance variables must be defined at the top of the class.

* If one function calls another, that is, if it is a dependent function, they must be defined close to each other.

* Functions that are conceptually close should be close to each other. This conceptual affinity may be direct, such as the dependency of functions or the use of variables by a function, or it may be due to the fact that it only performs similar operations.

* In dependent functions, the called function must be just below the calling function.

Codes should not be too long horizontally, the reader should never shift the line to the right.

We can use horizontal white space to relate things that are strongly related and separate things that are weaker.

We can also use white space to indicate the precedence of operators.

Source codes have a hierarchy. This hierarchy continues in the form of a class in a file, functions in a class, and code blocks in functions. Indents are required to make this hierarchy easier to read. Each element of the hierarchy is aligned from top to bottom, one indent to the right. Programmers also rely on it to read the code.

In very short functions, loops, or conditional structures, indentation is often ignored. No matter how short, we have to be careful.

Also, in for and while loops, there may be cases where the body part is dummy. In this case, the dummy body must also be properly indented.

If we are working with a team, all these formatting rules should be determined together and the same structure should be used for consistency.
#Chapter 6: Objects and Data Structures
Hiding Implementation is not just putting a layer between functions and variables. Hiding Implementation is actually an abstraction. It exposes abstract interfaces that allow users to manipulate data without knowing the implementation.

Objects hide data behind abstraction and provide functions to manipulate data. Data structure expose their data and have no meaningful functions. They are virtual opposites.

Procedural code uses data structures and makes it easy to add new functionality without changing existing data structures. Object Oriented code makes it easy to add new classes without changing existing functions. So what is difficult for one is easy for another.

There is a well-known heuristic called the Law of Demeter that says a module should not know about the innards of the objects it manipulates.

Violating the Law of Demeter will be far less confusing if data structures have global variables and no functions, and objects have private variables and public functions. This confusion sometimes leads to unfortunate hybrid structures that are half object and half data structure. But this is worst because makes it hard to add new function and also make it hard to add new data structures.

The concise form of a data structure is a class with public variables and no functions. This is also called a data transfer object, it is especially used in communication with the database. They take part in transforming the raw data in the database into objects in the application code.

If we want flexibility in adding new data types, we should prefer objects. If we want flexibility in adding new behaviors, we should prefer data structures and procedures. A good software developer should be able to determine his needs well and make a good choice.
#Chapter 7: Error Handling
While the program is running, things can go bad for various reasons, we are responsible for all of this and we should handle it.

In previous years, when there were no exceptions, when there was a problem, error codes were returned and then immediately checked. However, this control could easily be forgotten. So now we use exceptions instead of returning error code. Also, thanks to error handling, error catching codes and actual working algorithm codes are separated from each other.

Each exception you throw should provide enough information to identify the source and location of an error. Create informative error messages where you will mention the failed operation and the type of error and pass them along with your exceptions.

By wrapping the API we use with our own generated error class, we can make sure it returns a common exception type and significantly simplify our code.

If we are using a third party API, we will have minimized the dependency when we wrap the API. If we start using another library in the future, we will be able to switch with minimal workload. It also makes testing the code easier to emulate Third Party calls, ie testing. The final advantage is that we don't have to be tied to a particular API design, we can work however we feel.

We can create a class to handle exceptions that may occur in the code. This is called SPECIAL CASE PATTERN, in which case it is not necessary to deal with exceptional behavior.

If you want to return NULL from a method, try throwing an exception or returning a SPECIAL CASE object instead. If you are calling a nullable method from a third party API, wrap it with the method that will throw an exception.

As bad as returning NULL from a method is, much worse is passing a NULL value into a method.

In most programming languages, there is no way to deal with an accidentally passed NULL value. The rational approach is to forbid passing NULL by default. When we do this, we can understand that a NULL value is an indication of a problem.

Clean code should also be robust. Therefore, if we see error handling as one of the things we need to do, we can write robust and maintainable codes.

#Chapter 8: Boundaries
While developing software, we can sometimes purchase third-party software or use open source software. This software will have a very wide range of uses offered to us. In order to make the code more readable and less misused, it would be more accurate to use it in a class we wrote, rather than using the result returned directly from the Public API.

Third-party API is hard to learn, harder to integrate, much harder to do both together. Instead of trying them in production, we can write tests to better explore third-party code.

Testing is important not only for this, but also for sustainability. In this way, we can also measure whether an improvement or a change in the third-party API affects our own system.

Change is something that happens all the time, and good software designs can keep up with change without much effort or investment. When we use Third-Party software, we must carefully determine whether we can keep up with the development. Therefore, rather than relying on something we cannot control; It's better to rely on something we can control.
















