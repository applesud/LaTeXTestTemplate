# LaTeX Test Template
This is a package (+template) that I made for creating tests with LaTeX.

It started out as me thinking "Hey, that revision looks pretty cool! Was that made in LaTeX?", then trying to recreate one of the questions for myself. Then I got carried away with endlessly tweaking the typesetting. Then I thought it would be fun to write a package to do it all more easily. This repository is the result of that fun work!

Note: The code for this is a mess of copy-pasted internet stuff, confused trial and error, and a tiny sprinkling of code that written with *some* understanding or intent.

## "Documentation"
**`question (environment): {number of marks}`**\
Produces a main question.

**`sub-question (environment): {number of marks (pass \undefined to hide)}`**\
Produces a sub-question. Should only be used inside a main question environment.
If it contains any sub-sub-questions, it would probably be a good idea to pass `\undefined` to hide the mark.

**`sub-sub-question (environment): {number of marks}`**\
Produces a sub-sub-question. Should only be used inside a sub-question environment.

**`longanswer (macro): {number of lines}`**\
Produces a certain number of horizontal lines (spanning linewidth, below the current line) for students to do working out in.

**`shortanswer (macro):`**\
Produces a one horizontal lines (spanning linewidth) for students to do working out in. It is equivalent to `\longanswer{1}`.\
Originally, the line drawn wouldn't start a new line, instead continuing from the last character + hspace to fill the current line. However, I got rid of that because I thought it made the whitespace look too inconsistent and patchy.

**`multiplechoice (environment):`**\
A custom list environment. Specify choices with `\item`.
