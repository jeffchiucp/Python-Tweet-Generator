### Tweet Generator
### Project Organization

**What are the key features of the application? Are these clearly separated into their own files, classes, and/or modules?**
- The application returns a set of randomly generated word(s) based on how often they show up from the source file. Though not its main functionality, it can also see how often a specific word shows up in a body of text, how many unique words there are, and print out a list of words and their occurrences.
- Each file is a module! It's separated into:
    -`app.py` - main script for my Flask Server, it uses other modules to generate sentences 
    -`cleanup.py` - module for cleaning up source text and generates corpus.txt
    - `histogram.py` - grabs a list of words from a body of text
    - `histogram_oop.py` - refactoring histogram class to Dictogram class which helps to generates the random_weighted_words
    - `sample.py` - handles all the percentage handling and creating a list of words+occurrences and makes a text file for it.
    - `markov_chain.py` - Markov model module generating tweet sentence word from generate_markov_model 

- In Progress Code
    - `tokenize.py` # module for creating lists of tokens from a text
    - `markov_chain.py` # Markov model module generating a sentence word
    - `app.py` # allows tweeter option 

**Are the names of files, modules, functions, and variables appropriate and accurate? Would a new programmer be able to understand the names without too much contextual knowledge?** 
- Yes. I think they are clearly separated after code review. 
Reader should see it with Clear, semantic variable names. The new programmer can understand and there's no need to go through the comments to understand my codes.


**What are the scopes of variables and are they appropriate for their use case? If there are global variables, why are they needed?**
- No globals, and each variable stays only where they're needed.
- It's good idea to scope my variable and see that they are appropriate to use. I did not have global variable in my code, and I avoid global variables. 

**Are the functions small and clearly specified, with as few side effects as possible?**
- Each thing mostly does one thing, so I'm mostly sure, yes. I can likely separate `histogram.py` to something that changes things into probability. 
The Side of effect:
-Changing the variables and outside of the scope.
-Our Solution to avoid the side affect is: 
- Make all of your function modular and make sure it does not pass it.

**Are there functions that could be better organized in an Object-Oriented Programming style by defining them as methods of a class?**
Yes.  Remove coupling with Dictogram and MarkovModel. Change class to MarkovChain


**Can files be used as both modules and as scripts?
Do modules all depend on each other or can they be used independently?**
- Yes. All modules should be usable without anything else.