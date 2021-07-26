*************************************
```
This is my notes on practical vim (2nd edition)
I will leave some hints and practical problems
```
*************************************
*************************************
Tip1:
Use the dot command
Task: delete the first two lines and indent till the end of the text

start code
```
Line one
Line two
Line three
Line four
```

end code
```
Line one
    Line two
        Line three
            Line four
```

solution: 1.use the >G to indent till the end of the text.
          2.use the . command to do the same thing..
          
*************************************
*************************************
Tip2:
"Don't repeat yourself"
Task: Append the ; at the end of each line of code

starter code
```
the_vim_way/2_foo_bar.js
var foo = 1
var bar = 'a'
var foobar = foo + bar
```

end code
```
the_vim_way/2_foo_bar.js;
var foo = 1;
var bar = 'a';
var foobar = foo + bar;
```
solution:use A to append at each end of the line, j to move down the . to do the same things.
*************************************
*************************************
//Link with Tip 30: what if we want to make it for 50 times
//Run Normal Mode Command Across a Range.

starter code
```
var foo = 1
var bar = 'a'
var baz = 'z'
var foobar = foo + bar
var foobarbaz = foo + bar + baz
```

end code
```
 var foo = 1;
var bar = 'a';
var baz = 'z';
var foobar = foo + bar;
var foobarbaz = foo + bar + baz;
```
Solution: 1. Use the Use the normal Ex command to exexute the dot command across a range of liens.
Solution: 2. Use the :%normal A;. "%"means that the range is the whole file.(From the beginning of the line automaitcally.
*************************************
*************************************
//Linked to the Tip 68
//Reapeat a Cahnge on Contiguous Lines
Task: Change the dot into curly braces and set the numbers to the uppper cases.

starter code
```
1. one
2. two
3. three
4. four
```

end code
```
1) One
2) Two
3) Three
4) Four
```
Solution: make the micro first find . use "f." then replace it with the "r)" use w~ to make the first letter upper case. play the micra with 3@q.

But what if you have an obticle?
starter code
task: Breack the obstacles of the thrid line and make a change.
```
1. one
2. two
// break up the monotony
3. three
4. four
```
end code
```
1) One
2) Two
// break up the monotony
3) Three
4) Four
```

*************************************
*************************************
Tip3:
Take One Step Back, Then Three Forward
task: surround the + with two spaces

start code
```
var foo = "method("+argument1+","+argument2+")";
```

end code
```
var foo = "method(" + argument1 + "," + argument2 + ")";
```

Solution: 1. delete the + sign then change with the " + "sign using s.
use ;. to repeat it.
          2. ; used to repeat the finding proceess.


*************************************
*************************************
Tip4, Reverse
task:Learn how to reverse if you go a step too far
```
Repeat Reverse
.      u        
;      ,        f{char} or t{char}
n      N        F{char} or T{char}
&      u
@x     u
```

*************************************
*************************************
Tip5:Find nad Reaplace by Hand
task:Replace the "copy" with evry "content"

starter code
```
...We're waiting for content before the site can go live......
...If you are content with this, let's go ahead with it......
...We'll launch as soon as we have the conte......
```

end code
```
...We're waiting for copy before the site can go live......
...If you are content with this, let's go ahead with it......
...We'll launch as soon as we have the conte......
```
solution: Use the * to search more easily and then use the cw to change the words.
          After that use the n. etc. to make changes.
*************************************
*************************************
// Linked Tip 90: Eyeball Each Substitution
tast: repalce content with the word copy

starter code
```
...We're waiting for content before the site can go live...
...If you are content with this, let's go ahead with it...
...We'll launch as soon as we have the content...
```

end code
```
...We're waiting for copy before the site can go live...
...If you are content with this, let's go ahead with it...
...We'll launch as soon as we have the content...
```
solution: 1. use the :%s to search
          2. use /content/copy/g to repalce
          3. use /gc to ask evry time we search

*************************************
*************************************
