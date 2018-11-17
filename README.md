# Chapter 2: Meaningful Names

#### Use Intension-Revealing Names

#### Avoid Disinformation

- Avoid `list` unless it's actually a `List`.

#### Make Meaningful Distinctions

- Avoid `**Data` or `**Info`, which are indistinct noise words like `a` or `the`.
 
#### Use Pronounceable names

#### Use Searchable Names

- Single-letter names can only be used as local variables inside short methods.
 
- The lengthof a name should correspond to the size of its scope.

#### Avoid Encodings

- Hungarian Notation
Avoid Hungarian Notation

- Member prefixes
Avoid Member Prefixes (`m_`)

- Interfaces and Implementations
Avoid `Interface` or `Implementation`
 
- Avoid Mental Mapping
Clarity is king.
- Class Names
Class names as Noun phrase.
Avoid words like `manager, data, processor, info` in the name of class.
- Method Names 
Method names as Verb phrase
 
#### Don't be cute
 - Say what you mean, mean what you say.
 
#### Pick One Word per Concept
 - Use consistent lexicon.
 - It's confusing to have `fetch, retrieve, get` as equivalent methods of different classes.

#### Don't pun
 - Avoid using the same word for two purposes.

#### Use Solution Domain Names
 - `Queue` is meaningful enough for programmers
 
#### Use Problem Domain Names

#### Add Meaningful Context

#### Don't Add Gratuitous Context
 - Shorter names are generally better than longer ones, so long as they are clear.
 
 
# Chapter3 Functions

#### Small!
- Blocks and Indenting: one-line long

#### Do one thing
- Sections within Functions: don’t divide

#### One level of abstraction per function
Make sure that the statements within our function are all at the same level of abstraction.

- reading code from top to bottom: the stepdown rule (top-down narrative)

We want every function to be followed by those at the next level of abstraction so that we can read the program, descending one level of abstraction at a time as we read down the list of functions.

#### Switch statements (exception of do-on-thing rule)

We can’t always avoid switch statements, but we can make sure that each switch statement is buried in a low-level class and is never repeated.

#### Use descriptive name

A long descriptive name is better than a short enigmatic name.

#### Function arguments
The ideal number of arguments for a function is zero (niladic). Next comes one (monoadic), followed closely by two (dyadic). 
Three or more arguments (triadic)  should be avoided where possible.

- Common Monadic forms

If a function is going to transform its input argument, the transformation should appear as the return value.

- Flag arguments

Flag arguments are ugly.

- Dyadic functions

- Triads

- Argument objects

When a function seems to need more than two or three arguments, it is likely that some of those arguments ought to be wrapped into a class of their own.

- Argument lists

- Verb and keywords

Choosing good names for a function can go a long way toward explaining the intent of the function and the order and intent of arguments. For example, assertEquals might be better written as assertExpectedEqualsActual(expected, actual).

#### Have no side effects
Side effects are lies. Your function promises to d one thing, but it also does other hidden things!

- Output arguments

A double-take on an argument that was actually an output rather than an input? No!

#### Command Query Separation
Functions should either do something or answer something, but not both at once. Either your function should change the state of an object, or it should return some information about that object.

#### Prefer Exceptions to returing error codes
- Extract try/catch blocks
- Error handling is one thing
- Error dependency magnet

#### Don’t repeat yourself
Duplication may be the root of all evil in software.

#### Structured programming


# Chapter4: Comments

Comments are at best a necessary evil. The proper use of comments is to compensate for our failure to express ourself in code.


#### Comments Do No Make Up for Bad Code

#### Explain Yourself in Code
It's simply a matter of creating a function that says the same thing as the comment you want to write.

- not
```
// Check to see ...
if some_flags and another_flag
```
- but

```
if checkSomething():
```

#### Good Comments
- Legal comments

Copyright and authorship statements are necessary and reasonable things to put into a comment at the start of each source file.

- Informative comments

It is better o use the name of the function to convey the information where possible.

```// format matched kk:mm:ss EEE, MMM dd, yyyy```

- Explanation of Intent

```// This is our best attempt to get a race condition by creating large number of threads.```

- Clarification

```assertTrue)a.compareTo(a) == 0);   // a == a```

- Warning of consequences

```// Don't run unless you have some time to kill.```

- TODO comments

```// TODO blah blah...
It is not an excuse to leave bad code in the system.
```

- Amplification

A comment may be used to amplify the importance of something that may otherwise seem inconsequential.

- Javadocs in Public APIs

If you are writing a public API, then you should certainly write good javadocs for it.


#### Bad Comments

Usually they are crutches or excuses for poor code or justifications for insufficient decisions, amounting to little more than the programmer talking to himself.

- Mumbling

```// No properties files means all defaults are loaded.```

Any comment that forces you to look in another module for the meaning of that comment has failed to communicate to you and is not worth the bits it consumes.

- Redundant comments

Is the comment certainly informative than the code itself?

```
// Processor delay for this component
int backgroundProcessorDelay = -1;
```

- Misleading commnts

A programmer makes a statement in his comments that isn't precise enough to be accurate.

- Mandated comments

It is just plain sillly to have a role that every fnction must have a javadoc, or every variable must have a comment.

- Journal comments

```
// Update XXX-XX
// Update YYY-YY ...
```

- Noisy comments

```
// Default constructor

// The day of the comnth.
int dayOfMonth

// Returns the day of the month.
// @return the day of the month.
```

- Scary noise

Javadocs can also be noisy.

- Don' use a comment when you can ue a function of variable

```
// Actions ///////////////////////////////////////////////////////
```
Use them very sparingly, or thay'll fall into the background noise and be ignored.

-Closing brace comments

```
} // while
```
If you want to comment on your closing braces, try to shorten your functions instead.

- Attributions and bylines

```// Added by Rick.```

- Commented-out code

*Don't do this!!*

- HTML comments

- Nonlocal information

If you must write a comment, then make sure it describes the code it appears near.

- Too much information

```// Toooooo long comments to be read easily.```

- Inobvous connection

- Function headers

```Short function don't need much dscription.```

- Javadocs in nonpublic code

- Example
