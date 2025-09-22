# Homework 2 Docs

## change-pros:
Change-pros focuses on how eliza addresses the user and itself. What pronounds does it use and how does it approach the user using different ones in different ways. The main ways I approached pronounds with eliza are:

#### Swap my and your
This one is simple, since your figuring our possessive pronouns, and is necessary when apporaching any common language
USAGE: Matches any sentence containing the pronouns my or yours and swaps the two

#### Swap me and you || Swap am and are
These two are quite different on the basis that theres no direct comparison for the 2nd person pronoun. Kept these two together on that basesis
USAGE: Matches any sentence containing the pronouns me and you || am and are and swaps the two

#### Swap mine and yours
Same idea as my and your, just pluralized
USAGE: Matches any sentence containing the pronouns mine and yours and swaps the two

#### Swap we and you
These ones are quite different on the idea that eliza needs to be able to swap between  plural definitions of i and you and mine and yours for special cases where eliza needs to talk to the person as if it's part of that persons'a gorup
USAGE: Matches any sentence containing the pronouns we and you || us and you || our and your || ours and yours and swaps the two

## database

Here, I wanted to go more in depth with the feelings and beliefs side of eliza, and see if it can dig deeper using those questions as starters:

#### Feelings
The 'you feel' statement should try to capture the user into reflection on the duration or how long they felt a feeling
USAGE: ...you feel (4) and eliza will fill in 4 for you  

The 'you are feeling' statement pushes the user to think about the underlying cause behind the emotions of that statement
USAGE: ...you are feeling (4) and eliza will fill in 4 for you 

The 'you are happy' statement tries to get the user to question what is the root cause of their happiness
USAGEL ...you are happy... and eliza will give you a basic response back

#### Beliefs
The 'believe' statement should get the user to question how they began to believe (4) in the first place
USAGE: ...believe (4) and eliza should fill in 4 for you

The 'doubt' statement should have the user question why they doubt (4) in the first place
USAGE: ...doubt (4) and eliza should fill in 4 for you