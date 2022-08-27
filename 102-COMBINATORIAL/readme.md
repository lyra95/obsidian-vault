# Introduction

My well written solutions for the book [102 Combinatorial Problems](https://rainymathboy.files.wordpress.com/2011/01/102-combinatorial-problems.pdf)

# Inline math text are not rendered; how to fix?

When `.md` files get translated to `.html` file, github fails to recognize some inline MathJax text.

I use [`tampermonkey`](https://addons.mozilla.org/en-US/firefox/addon/tampermonkey/) to fix it. My script is hacky, but you might use [it](https://gist.github.com/lyra95/f237e0954a5a54985493f40e0fe9c747)


# Problems Grouped By Keywords

## two-sides

A quantity than has more that two interpretation

```dataview
TABLE dificulty, rating FROM "102-COMBINATORIAL/advanced" WHERE two-sides=true
```

## custom-operation

Define an operation to make the idea concrete

```dataview
TABLE dificulty, rating FROM "102-COMBINATORIAL/advanced" WHERE custom-operation=true
```
