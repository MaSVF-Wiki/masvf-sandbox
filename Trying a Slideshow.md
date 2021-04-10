# Trying a Slideshow
_(a title page)_

---

# First Page
To view this page as a slideshow in Obsidian, enable the [Slides plugin](https://help.obsidian.md/Plugins/Slides) in Core Plugins, then right-click on the filename in the left sidebar, or use the three-dot menu in the upper right corner. (There is also a "Start presentation" hotkey you can assign.)

Or, use one of the tools from this [nice list of markdown presentation tools](https://gist.github.com/johnloy/27dd124ad40e210e91c70dd1c24ac8c8).

---
## Second Page
(Using an H2 header instead of an H1)

This is the wonderful and amazing _second page._

---
# Third Page
## This is a second-level header
- with some
- bullets
- and a wiki link: [[Static Site Generators]]
	- which seems to go nowhere in presentation mode

---
# Fourth Page

some nice, preformatted lines:

```
(def lazy-fib
  (concat
   [0 1]
   ((fn rfib [a b]
        (lazy-cons (+ a b) (rfib b (+ a b)))) 0 1)))
```

---
- this page is
- Just Bullets
- it looks like
- no Reveal.js styling
- in Obsidian Slides plugin
- (maybe I'm wrong)

---
## Obligatory Table

First Header | Second Header
------------ | ------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column

_ref: [Format your notes (Tables)](https://help.obsidian.md/How+to/Format+your+notes#Tables)_

---
# Final Page
The End.
Come back soon!

 -- [[Peter Kaminski]]