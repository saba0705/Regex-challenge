Regex Tutorial to match an email

Introductory paragraph

This tutorial is going to explain the use of regex to match emails using the expression /^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/. This can be useful when validating emails using applications/technologies such as Node (Inqurier) or MongoDB.

A regular expression is a sequence of characters that defines a search pattern. This is commonly used to find patterns within a string, find/replace characters within a string or validate input. This tutortial will go walk through the components of a regex and how it applies to matching an email.

Table of Contents

Anchors Quantifiers OR Operator Character Classes Flags Grouping and Capturing Bracket Expressions Greedy and Lazy Match Boundaries Look-ahead and Look-behind Regex Components

Anchors The $ anchor signifies a string that ends with the characters that precede it. Just as with the ^ character, it can be preceded by an exact string or a range of possible matches.

Quantifiers Quantifiers in this regex includes the + operator, which will connect the users email name + email service + .com. Another quantifier for this regex includes {2,6}, which will allow a match range of 2-6 characters for the character set of [a-z.].

OR Operator The OR operator (|) is used to match one pattern or another. Example: cat|dog matches either cat or dog. In other contexts, the OR operator can be used to specify alternate acceptable patterns.

Character Classes The character class in this expression is \d, which matches a single characters that is a digit from 0-9. It will only match a single digit such as "4", but not "44".

Flags Flags modify the behavior of the regex.

i makes the regex case-insensitive.
g makes the regex global, meaning it will find all matches rather than stopping after the first match.
m makes the regex multiline, allowing ^ and $ to match the start and end of each line. Although flags are not used in our specific email regex, they can be very useful for other regex patterns.
Grouping and Capturing Capturing group #1 in this expression is ([a-z0-9_.-]+) that matches the user email name. The second capturing group is ([\da-z.-]+) which will match the email service. Then lastly, capture group #3 is ([a-z.]{2,6}) to capture the .com.

Bracket Expressions Bracked expressios for email validation includes the character sets of [a-z0-9_.-], which is matching any letter a-z and is case senstive. It also matches a character 0-9 and matches the characters "_" , "-" , and "."; [\da-z.-], which is matching a single digit from 0-9, any character a-z (case senstive), and the characters "." and "-".; [a-z.] matches any character a-z(case senstive) and the character ".".

Greedy and Lazy Match This regrex includes greedy matches. Since it includes the + Quantifier, it will match as many times as possible giving back as needed. Another greedy Quantifier used in this regex is {} when matching `{2,6} for the last capture group.

Boundaries Boundaries assert positions in the string.

\b matches a word boundary.
\B matches a position that is not a word boundary. In our email regex, boundaries are not explicitly used, but they can be essential in other contexts to ensure matches occur at specific word boundaries.
Look-ahead and Look-behind A regular expression generally matches from left to right. This is why lookahead and lookbehind assertions are called as such — lookahead asserts what's on the right, and lookbehind asserts what's on the left.

Summary Let's break down the regular expression /^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/ used for email validation step by step:

'^': Asserts the position at the start of a line. This ensures that the entire string will be matched from the beginning.

'([a-z0-9_.-]+)':
'(' and ')' create a capturing group for the local part of the email (before the @).
'[a-z0-9_.-]' is a character class that matches any lowercase letter (a-z), digit (0-9), underscore (_), dot (.), or hyphen (-).
'+' means one or more of the preceding character class. This ensures that the local part has at least one character.
'@': Matches the @ symbol literally.

'([\da-z.-]+)':
'(' and ')' create another capturing group for the domain part of the email (between the @ and the final dot).
'[\da-z.-]' is a character class that matches any digit (\d), lowercase letter (a-z), dot (.), or hyphen (-).
'+' means one or more of the preceding character class. This ensures that the domain part has at least one character.
'.': Matches the dot . symbol literally. It needs to be escaped with a backslash because a dot in regex means "any character".

'([a-z.]{2,6})':
'(' and ')' create another capturing group for the top-level domain (TLD) part of the email (after the final dot).
'[a-z.]' is a character class that matches any lowercase letter (a-z) or dot (.).
'{2,6}' specifies that the preceding character class should be matched at least 2 times and at most 6 times. This ensures that the TLD has between 2 and 6 characters.

'$': Asserts the position at the end of a line. This ensures that the entire string will be matched up to the end.

Putting it all together, this regular expression will match a string that starts with one or more lowercase letters, digits, underscores, dots, or hyphens, followed by an @ symbol, followed by one or more digits, lowercase letters, dots, or hyphens, followed by a dot, and ends with a TLD that is between 2 and 6 characters long, consisting of lowercase letters or dots.

Author This tutorial was created by Saba Pervez a Full stack developer bootcamp student. To view my projects please visit: https://github.com/saba0705
