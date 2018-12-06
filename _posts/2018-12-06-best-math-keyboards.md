---
layout: post
title:  "The best keyboard and key layout for mathematicians"
date:   2018-12-06
---

### The best keyboards and keyboard layouts for mathematicians

## Most commonly used symbols in a LaTeX document

Lets start by looking at the most commonly used symbols in a standard
latex document. I got some new papers from arxive and downloaded the source.
I wrote a small programm charfreq.py to check the character frequency:

```python
#!/usr/bin/python3
import sys
from collections import Counter
text = sys.stdin.read()
counts = Counter(text)
counts = sorted(counts.items(), key=lambda t : (t[1],t[0]))
print(counts)
```

Then feed it some latex file:
```shell
cat somefile.tex | ./charfreq.py
```

This outputs some nice statistic and tells me that the most frequently used letters are:

|Letter|Frequency|
|------|---------|
|space |6983|
|\\ |2551|
|a|1970|
|e|1444|
|}|1308|
|{|1308|
|r|1195|
|(|1089|
|)|1088|
|t|1059|
|p|971|
|c|908|
|o|872|
|n|821|
|newline|816|
|i|773|
|s|738|
|,|692|
|d|625|
|l|608|
|f|584|
|2|567|
|x|539|
|h|494|
|k|439|
|y|434|
|g|425|
|b|417|
|$|374|
|-|328|
|||300|
|m|284|
|0|268|
|1|243|
|z|238|
|q|233|
|=|227|
|^|188|
|_|186|
|+|186|
|u|184|
|w|158|
|.|136|
|]|112|
|[|112|
|/|103|
|%|103|
|&|90|
|S|87|
|;|81|
|:|72|
|'|63|
|v|51|
|L|51|
|D|50|
|F|47|
|C|44|
|*|40|
|X|37|
|T|37|
|P|36|
|A|32|
|N|31|
|5|30|
|4|30|
|B|26|
|#|26|
|R|23|
|I|22|
|3|21|
|>|19|
|!|18|
|<|16|
|O|15|
|W|14|
|M|13|
|9|10|
|8|9|
|7|9|
|6|9|
|j|5|
|Z|5|
|Y|4|
|H|3|
|G|3|
|E|3|
|V|1|
|U|1|



Text can be **bold**, _italic_, or ~~strikethrough~~. [Links](https://github.com) should be have dotted underlines and solid underlines on hover.

There should be whitespace between paragraphs. There should be whitespace between paragraphs. There should be whitespace between paragraphs. There should be whitespace between paragraphs.

There should be whitespace between paragraphs. There should be whitespace between paragraphs. There should be whitespace between paragraphs. There should be whitespace between paragraphs.

> There should be no margin above this first sentence.
>
> Blockquotes should be a italicized with a gray border along the left side.
>
> There should be no margin below this final sentence.

# Heading 1

This is a normal paragraph following a Heading. Bacon ipsum dolor sit amet t-bone doner shank drumstick, pork belly porchetta chuck sausage brisket ham hock rump pig. Chuck kielbasa leberkas, pork bresaola ham hock filet mignon cow shoulder short ribs biltong.$x^2$

## Heading 2

This is a normal paragraph following a Heading. Bacon ipsum dolor sit amet t-bone doner shank drumstick, pork belly porchetta chuck sausage brisket ham hock rump pig. Chuck kielbasa leberkas, pork bresaola ham hock filet mignon cow shoulder short ribs biltong.


> This is a blockquote following a Heading. Bacon ipsum dolor sit amet t-bone doner shank drumstick, pork belly porchetta chuck sausage brisket ham hock rump pig. Chuck kielbasa leberkas, pork bresaola ham hock filet mignon cow shoulder short ribs biltong.

This is a normal paragraph following a Heading. Bacon ipsum dolor sit amet t-bone doner shank drumstick, pork belly porchetta chuck sausage brisket ham hock rump pig. Chuck kielbasa leberkas, pork bresaola ham hock filet mignon cow shoulder short ribs biltong.


### Heading 3

```
This is a code block following a Heading.
```

#### Heading 4

* This is an unordered list following a Heading.
* This is an unordered list following a Heading.
* This is an unordered list following a Heading.

##### Heading 5

1. This is an ordered list following a Heading.
2. This is an ordered list following a Heading.
3. This is an ordered list following a Heading.

###### Heading 6

| What      | Follows         |
|-----------|-----------------|
| A table   | A Heading        |
| A table   | A Heading        |
| A table   | A Heading        |

----------------

There's a horizontal rule above and below this.

----------------

Here is an unordered list:

* Salt-n-Pepa
* Bel Biv DeVoe
* Kid 'N Play

And an ordered list:

1. Michael Jackson
2. Michael Bolton
3. Michael Bublé

And a nested list:

* Jackson 5
  * Michael
  * Tito
  * Jackie
  * Marlon
  * Jermaine
* TMNT
  * Leonardo
  * Michelangelo
  * Donatello
  * Raphael

Definition lists can be used with HTML syntax. Definition terms are bold and italic.

<dl>
    <dt>Name</dt>
    <dd>Godzilla</dd>
    <dt>Born</dt>
    <dd>1952</dd>
    <dt>Birthplace</dt>
    <dd>Japan</dd>
    <dt>Color</dt>
    <dd>Green</dd>
</dl>

----------------

Tables should have bold headings and alternating shaded rows.

| Artist            | Album           | Year |
|-------------------|-----------------|------|
| Michael Jackson   | Thriller        | 1982 |
| Prince            | Purple Rain     | 1984 |
| Beastie Boys      | License to Ill  | 1986 |

If a table is too wide, it should condense down and/or scroll horizontally.

| Artist            | Album           | Year | Label       | Awards   | Songs     |
|-------------------|-----------------|------|-------------|----------|-----------|
| Michael Jackson   | Thriller        | 1982 | Epic Records | Grammy Award for Album of the Year, American Music Award for Favorite Pop/Rock Album, American Music Award for Favorite Soul/R&B Album, Brit Award for Best Selling Album, Grammy Award for Best Engineered Album, Non-Classical | Wanna Be Startin' Somethin', Baby Be Mine, The Girl Is Mine, Thriller, Beat It, Billie Jean, Human Nature, P.Y.T. (Pretty Young Thing), The Lady in My Life |
| Prince            | Purple Rain     | 1984 | Warner Brothers Records | Grammy Award for Best Score Soundtrack for Visual Media, American Music Award for Favorite Pop/Rock Album, American Music Award for Favorite Soul/R&B Album, Brit Award for Best Soundtrack/Cast Recording, Grammy Award for Best Rock Performance by a Duo or Group with Vocal | Let's Go Crazy, Take Me With U, The Beautiful Ones, Computer Blue, Darling Nikki, When Doves Cry, I Would Die 4 U, Baby I'm a Star, Purple Rain |
| Beastie Boys      | License to Ill  | 1986 | Mercury Records | noawardsbutthistablecelliswide | Rhymin & Stealin, The New Style, She's Crafty, Posse in Effect, Slow Ride, Girls, (You Gotta) Fight for Your Right, No Sleep Till Brooklyn, Paul Revere, Hold It Now, Hit It, Brass Monkey, Slow and Low, Time to Get Ill |

----------------

Code snippets like `var foo = "bar";` can be shown inline.

Also, `this should vertically align` ~~`with this`~~ ~~and this~~.

Code can also be shown in a block element.
````
var foo = "bar";
````

Code can also use syntax highlighting.
````Javascript
var foo = "bar";
````

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```Javascript
var foo = "The same thing is true for code with syntax highlighting. A single line of code should horizontally scroll if it is really long.";
```

Inline code inside table cells should still be distinguishable.

| Language    | Code               |
|-------------|--------------------|
| Javascript  | `var foo = "bar";` |
| Ruby        | `foo = "bar"`      |

----------------

Small images should be shown at their actual size.

![](http://placekitten.com/g/300/200/)

Large images should always scale down and fit in the content container.

![](http://placekitten.com/g/1200/800/)

```
This is the final element on the page and there should be no margin below this.
```
<!-- %enddocs -->

## License

[MIT](./LICENSE)
