'''
This is my notes on practical vim (2nd edition)
I will leave some hints and practical problems
''''

Tip1:
Use the dot command
Task: delete the first two lines and indent till the end of the text

start code
'''
Line one
Line two
Line three
Line four
'''

end code
'''
Line one
    Line two
        Line three
            Line four
'''


solution: 1.use the >G to indent till the end of the text.
          2.use the . command to do the same thing..
          
Tips2:
"Don't repeat yourself"
Task: Append the ; at the end of each line of code

'''
the_vim_way/2_foo_bar.js
var foo = 1
var bar = 'a'
var foobar = foo + bar
'''

'''
the_vim_way/2_foo_bar.js;
var foo = 1;
var bar = 'a';
var foobar = foo + bar;
'''

