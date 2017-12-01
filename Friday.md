# Sandi Metz

"On the unhappiness of Software Developers"
Persuasion is the reason why some people are unhappy.
"Influence, The Pscyhology of Persuasion" by Robert Cialdini
1. Reciprocity, if you give something to someone they feel obliggated to give something back. Sometimes more of that something.
2. consistency
3. Social Proof. If a person doesn't know what to do in a situation they will do what others are doing.
4,5,6. Authority, Liking, scarcity.
"How to win friends & Influence People" - Dale Carnegie
Act like othe rpeople are interesting, and eventually they will be so.

Psychological Safety is compared of
* Conversational Equality - people in general speak the same amount.
* Average Social Sensability - people can tell how others feel w/o verbal cues

This is what makes a good team.

# Aaron Patterson 

The greatest part of this talk was how Aaron got super famous in Japan for a day. He did a lightning talk about it at the end.
He also gave a snippet of code to dump the ObjectSpace after loading the rails environment, which can be useful for assessing memory size.

# What does the GIL really give you? Daniel Vartanov

This guy had great slides. I'm not sure what software he used for his code evaluation but it was awesome.
When MRI switches between threads it's called context switching.
Ruby will switch threads everytime a method is called.
GIL is not here for your convenience, it is for the convenience of MRI developers.

# JIT Compiler - k0kubun

JIT is Just-in-time commpiler.
Ruby gets parsed into a parser which gets written to bytecode.
Runs within a stack-based ruby VM.
github.com/k0kubun/yarv-mjit

