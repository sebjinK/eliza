# Homework 2 Docs

## Analysis Paragraph
Overall, I think i followed some of the necessary rules for eliza to function well.When it comes to pattern matching for the topics and words I do cover, Eliza works very well. Near perfect for a regular bot. And generally, I think that's good for eliza. The bot has a lot of potential when applied as a mini-general service bot that can talk to patients with limited wording. It also helps as a way to keep someone mildly engaged especially when they're dealing with the feeling of not being heard.

But I think the overall presentation is held back by a lack of proper responses to many of the topics that couold come up. I didn't include any proper responses to slang or internet type vocab that would pop up like normal text when you are typing. Having to keep track of it all would be a likely nightmare, and not one I want to go through when hardcoding Eliza's responses like this. As an example, many of the lmao or "are you a dog" questions got hit with a "could you expand on that" because it didn't know how to properly code it

Eliza should be more considerate of the presentation of words against each other. Whilst the pattern matching is great, a good next step would be to have it recognize the previous comment as "context" and build up context over time. Of course, having eliza analyze all of that previous context would be highly intensive computationally, but I think having it could make the design process much easier than just hard-coding in all of the words or phrases I want eliza to keep people distracted with. 

## Getting started
Best if you start on a linux distro, i would install clisp (sudo apt install clisp for ubuntu) and then to run it:
> clisp
> (load "eliza_starter.lisp")
## To use eliza: 
> (eliza '([WHAT YOU ARE GOING TO SAY]))
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

## database and keywords

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

#### causality
The 'causality' statement has the user question whether or not they are properly considering the validtiy of their reasoning
USAGE: ...believe and eliza will give a plain response

#### absolutes
The 'always' statement should give user a questioning experience about when something DIDN'T happen
USAGE: ...always (4) and eliza will restate 4 to you

The 'never' statement should make the user consider that 4 does sometimes happen
USAGE: ...never (4) and eliza will restate 4 to you

#### ability / blockage
The 'can't' statement should only allow the user to believe that they are considerate of their siutation
USAGE: ...can't (4) and eliza will restate 4 to you

The ‘couldn’t’ statement should help the user reflect on what barriers kept them from doing (4).
USAGE: …couldn’t (4) and Eliza will restate (4) back to you, asking what stopped you.

#### time 
The ‘late’ statement should reassure the user that being late is not final and encourage them to move forward.
USAGE: …late and Eliza will give a plain supportive response.

The ‘early’ statement should get the user to explain their motivation for being early to (4).
USAGE: …early (4) and Eliza will restate (4) back to you, prompting for a reason.

#### Defaults
Statements randomized to switch between when we say something eliza doesn't expect

