## Description
A giant stash of powerful weapons and gear have been dropped into the arena - but there's one item you have in mind. Can you filter through the stack to get to the one thing you really need?
## Difficulty
Very easy
## Steps to Flag
**Note:  
Always use ```strings``` first to do basic triage**
1. Download the challenge and the program look like this.
```
┌──(kali㉿kali)-[~/HTBTryout/LootStash]
└─$ ls
rev_lootstash  rev_lootstash.zip


┌──(kali㉿kali)-[~/HTBTryout/LootStash/rev_lootstash]
└─$ ./stash
Diving into the stash - let's see what we can find.
.....
You got: 'Glimmer, Prophecy of Magic'. Now run, before anyone tries to steal it!

                                                                                           
┌──(kali㉿kali)-[~/HTBTryout/LootStash/rev_lootstash]
└─$ ./stash
Diving into the stash - let's see what we can find.
.....
You got: 'Shadowfeather, Legacy of the Dead'. Now run, before anyone tries to steal it!
```
2. Looks like random names will be printed everytime.  
3. Use strings to find the flag.
```             
┌──(kali㉿kali)-[~/HTBTryout/LootStash/rev_lootstash]
└─$ strings -n 20 stash | grep "HTB{"

HTB{n33dl3_1n_a_l00t_stack}
```
**Flag:**
```
HTB{n33dl3_1n_a_l00t_stack}
```
**Note:  
Didnt thought of using strings from the start.  
Went to use ghidra to analyse and thought of writing script.  
Thought it was similar to previous challenge.**
