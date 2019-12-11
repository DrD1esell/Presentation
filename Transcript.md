Hello, my name is Yauhen Kalanitski and this is my presentation

Sometimes we need to find some character combinations in text or check if some text fits to pattern. For example, our application admits user's phone number only in this format. How to check this? We can use next function. But this is a big unreadable piece of code. Also we can use this short, but weird function. It’s weird only if you don't know the regular expression technology.
In computing, a regular expression, also referred to as "regexp" or "regex", provides a concise and flexible means for matching strings of text, such as particular characters, words, or patterns of characters. A regex is written in a formal language that can be interpreted by a regex processor.
In it's simplest form, a regex is a string of symbols to match "as is". That's not very impressive yet. But you can see that regexes match the first case found, once, anywhere in the input string.
So what if you want to match several characters? You need to use a quantifier. The most important quantifiers are asterisk, plus and question mark. 
Quantifiers take the preceding character as argument and attempt to match it zero, one or more times. So, ``x`` and asterisk will match zero or more x's, ``x`` and plus will match one or more x's and ``x`` and question mark will match exactly one x or none at all. By default, regexes are greedy. They take as many characters as possible. In the next example, you can see that the regex matches as many x's as there are.
Also we can define number of occurences in curly braces.
n in curly braces matches exactly n occurrences of the preceding expression.
n and a comma matches at least n occurrences of the preceding expression.
n comma m matches at least n and at most m occurrences of the preceding expression.

A lot of special characters are available for regex building. Here are some of the more usual ones.
- ``.`` 	The dot matches any single character.
- ``\d``	Matches a digit.
- ``\D``	Matches a non-digit.
- ``\w``	Matches an alphanumberic character.
- ``\W``	Matches a non-alphanumberic character.
- ``\s``	Matches a whitespace character.
- ``\S``	Matches a non-whitespace character.
- ``\n``	Matches a newline character.

	
If you need to use any of the special characters literally (actually searching for a ``*``, for instance), you must escape it by putting a backslash in front of it. For instance, to search for ``a`` followed by ``*`` followed by ``b``, you'd use ``/a\*b/``—the backslash "escapes" the ``*``, making it literal instead of special.

``^`` and ``$`` are important to regexes. Without them, regexes match anywhere in the input. With ``^`` and ``$`` you can make sure to match only a full string, the beginning of the input, or the end of the input.

You can group characters by putting them between square brackets. This way, any character in the class will match one character in the input.
``[abc]``	Match any of ``a``, ``b``, and ``c``.
``[^abc]``	A caret ``^`` at the beginning indicates "not". In this case, match anything other than ``a``, ``b``, or ``c``.
``[a-z]``	Match any character between ``a`` and ``z``.

Parentheses around any part of the regular expression pattern causes that part of the matched substring to be remembered. Once remembered, the substring can be recalled for other use.
For example, this pattern  illustrates additional escaped and special characters and indicates that part of the pattern should be remembered. It matches precisely the characters 'Chapter ' followed by one or more numeric characters. parentheses are used to remember the first matched numeric characters after word Chapter.

In JavaScript, regexes are used with the exec and test methods of RegExp, and with the match, matchAll, replace, search, and split methods of String.
When you want to know whether a pattern is found in a string, use the test or search method; for more information (but slower execution) use the exec or match methods. If you use exec or match and if the match succeeds, these methods return an array and update properties of the associated regex object and also of the predefined regular expression object, RegExp. If the match fails, the exec method returns null (which coerces to false).

Regular expressions have optional flags that allow for functionality like global and case insensitive searching. These flags can be used separately or together in any order, and are included as part of the regular expression.

- ``g``	Global search. This means that regex search all occurences in text, not only first one
- ``i``	Case-insensitive search.
- ``m``	Multi-line search. In this case signs caret and dollar mark mathes beginning and ending of lines

The above is in no way a complete description of regexes. There are more ways to write them, more special characters, and more quantifiers available. What's available depends also on the implementation. In case you're interested in learning a more complete set of regexes, see the docs on MDN. 
Thanks for attention)
