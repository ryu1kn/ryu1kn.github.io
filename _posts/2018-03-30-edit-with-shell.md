---
layout: post
title:  Leverage shell commands to quickly edit text on Visual Studio Code
date:   2018-03-30 12:35:58 +1100
categories: blog
---

I really like vi. When I started using Visual Studio Code as my main editor shortly after it hit version 1, one thing I felt missing in Code was the ability to quickly edit text using various commands already available on your shell. For example, let's say you're editing a section of text that has the following list of contributors.

```
Contributors:

    - Mike, 3 PRs
    - Elizabeth, 5 PRs
    - Robert, 2 PRs
    - Mary, 10 PRs
```

If you want to order them by the amount of contributions, in vi, you can utilise shell's `sort` command:

1. Select the list of contributors
1. Press `:` to go to the visual mode (which shows `:'<,'>` on the command line)
1. Type `!` followed by normal shell command `sort -t, -k 2 -n -r` and hit the enter key

Then you'll get

```
Contributors:

    - Mary, 10 PRs
    - Elizabeth, 5 PRs
    - Mike, 3 PRs
    - Robert, 2 PRs
```

If you want to drop the number of PRs from the list, you can in addition use `cut` command followed by pipe `|`,
i.e. Enter `! sort -t, -k 2 -n -r | cut -d, -f1`

```
Contributors:

    - Mary
    - Elizabeth
    - Mike
    - Robert
```

You can leverage all the powerful commands available on your shell! And, this is exactly what
[Edit with Shell Command extension](https://marketplace.visualstudio.com/items?itemName=ryu1kn.edit-with-shell)
offers you on Code; Editing selected text with commands available on your shell.

You can also just insert shell commands output at the cursor position instead of modifying text in the editor.

If you often come across situations where you feel, "it would be a piece of cake if I can use blah command", give the extension a try on your Code!!
