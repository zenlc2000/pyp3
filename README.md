#The Python3 Pyed Piper

**Note:** All respect to original author Toby Rosen of Sony Imageworks. This page is the first section from https://code.google.com/archive/p/pyp/

     ls | pyp "p.replace('maybe','yes') | pp.sort() | pp[1:3] |p , p , p.strip('abc') | whitespace | p[3], 'no' | p.upper() "

##Piping Python Through Pipes

Pyp is a linux command line text manipulation tool similar to awk or sed, but which uses standard python string and list methods as well as custom functions evolved to generate fast results in an intense production environment. Pyed Pyper was developed at Sony Pictures Imageworks to facilitate the construction of complex image manipulation "one-liner" commands during visual effects work on Alice in Wonderland, Green Lantern, and the The Amazing Spiderman.

Because pyp employs it's own internal piping syntax ("|") similar to unix pipes, complex operations can be proceduralized by feeding the output of one python command to the input of the next. This greatly simplifies the generation and troubleshooting of multistep operations without the use of temporary variables or nested parentheses. The variable "p" represents each line as a string, while "pp" is entire input as python list: \> ls | pyp "p[0] | pp.sort() | p + ' first letter, sorted!'" #gives sorted list of first letters of every line

In practice, the ability to easily construct complicated command sequences can largely replace "for each" loops on the command line, thus significantly speeding up work-flow using standard unix command recycling.

pyp output has been optimized for typical production scenarios. For example, if text is broken up into an array using the "split()" method, the output will be automatically numbered by field making selecting a particular field trivial. Numerous other conveniences have been included, such as an accessible history of all inter-pipe sub-results, an ability to perform mathematical operations, and a complement of variables based on common metacharcter split/join operations.

For power users, commands can be easily saved and recalled from disk as macros, providing an alternative to quick and dirty scripting. For the truly advanced user, additional methods can be added to the pyp class via a config file, allowing tight integration with larger facilities data structures or custom toolsets.
