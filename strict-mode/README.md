# Strict Mode

JavaScript is a language with a long history. Some websites were written using JavaScript almost 30 years ago, and many people are still using browsers that don't support modern JS features like `let`, `const` or `() => {}`.

As JavaScript applications grow larger more complex, and as browsers become more powerful JavaScript has added new features that help developers write better code. But because of it's legacy JavaScript cannot remove features from the language.

So, _strict mode_. Strict mode effectively turns any code below that line into "JavaScript 2.0", enforcing and good practices while throwing errors when you try to use older insecure features or bad practice. This compromise allows old websites to continue working, while at the same time letting developers write new code with more security.

- [javascript.info](https://javascript.info/strict-mode)
- [mdn: strict mode](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Strict_mode)
- [mdn: sloppy mode](https://developer.mozilla.org/en-US/docs/Glossary/Sloppy_mode)

---

## Keep it Simple

You should always use strict mode.

Trying to learn two different JavaScripts ("strict" and "sloppy") will only make things more complicated. And there's no good reason to be using the "sloppy" mode features anyway, there's a reason they were restricted.

---

## Undeclared Variables

Of all the differences between "strict" and "sloppy" mode, the most important for you right now is undeclared variables:

```js
undeclaredVariable = 'hello'; // no error! not in strict mode
```

```js
'use strict';

undeclaredVariable = 'hello'; // ReferenceError
```

It's likely that you will come across some confusions with this difference if you are running code directly in your browser's console, in node or if you are using another online environment like repl.it.

---

## Study Environments

- **JS Tutor** uses strict mode by default, there is no way to turn it off. This means that you cannot use that website to explore the differences between "strict" and "sloppy" JS.
- **Study Lenses** can run code in both "strict" and "sloppy" mode. The simplest way to run code in strict mode is to write `'use strict';` at the top of each file, all .js files in Debugging have this. You can also use strict mode without typing `'use strict';` by enabling the `environment` option and turning on `strict`. All code in Welcome to JS was run in strict mode using this option to keep the code simpler in your first weeks.
