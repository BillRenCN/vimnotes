*************************************
```
This is my notes on practical vim (2nd edition)
I will leave some hints and practical problems
```
*************************************
*************************************
Tip 1:
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
Tip 2:
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
Tip 3:
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

Solution: 1. delete the + sign then change with the " + "sign using s command which stands for substitiude.After that use ;. to repeat it.
          2. ; used to repeat the finding proceess.


*************************************
*************************************
Tip 4, Reverse
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
Tip 5:Find nad Reaplace by Hand
task:Replace the "copy" with every "content"

starter code
```
...We're waiting for content before the site can go live...
...If you are content with this, let's go ahead with it...
...We'll launch as soon as we have the conte...
```

end code
```
...We're waiting for copy before the site can go live...
...If you are content with this, let's go ahead with it...
...We'll launch as soon as we have the conte...
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
Tip 6: Meet the Dot Formula
Task: review the tips from 1 to 5, find the main idea

```
One keystroke to Move, One Keystroke to Execute.
```

*************************************
*************************************
Tip 7: Pause with Your Brush Off the Page 

```
You're not a programmer, You are an artist.
```

*************************************
*************************************
Tip 8: Chunk Your Undos

```
Use the <Esc> + o instesd of <CR> will be useful if you need undo commands.
```

*************************************
*************************************
Tip 9: Compose Repeatable Changes

task: Your cursor is positioned on the "h" at the end of this line of the text, you want to delete the word "nigh".

start code
```
The end is nigh
```

end code
```
The end is
```

solution1: use "db" to delete backwords, after that use "x" to delete the rest h character.
solution2: use "b" to to backwords, after that use db to delete a word.
solution3: use "daw" to delete an entire word.

*************************************
*************************************
//Related Tip52: Trace Your Selection with Precision Text Objects

task: Change the {url} to "#" and the {title} to "click here"

start code
```
var tpl = [
    '<a href="{url}">{title}</a>'
]
```

end code
```
var tpl = [
    '<a href="#">click here</a>'
]
```
solution: use "ci#" command to change inside the double quotes. After that use the cit to change in the tags.

*************************************
*************************************
Tip 10: Use Counts to Do simple Arithmetic

task: 

knowlege: <C-a> and <C-x> commands perform 10 addition and subtraction on numbers.

start code
```
.blog, .news { background-image: url(/sprite.png); }
.blog { background-position: 0px 0px }
```

end code
```
.blog, .news { background-image: url(/sprite.png); }
.blog { background-position: 0px 0px }
.news { background-position: 180px 0px }
```
solution: 1. Use the yy to yank the entire line
          2. Use p to paste to the next line
          3. Use cW to change a hole chunck of word
          4. Use <C-x>180 to substract 180 of the first 0

