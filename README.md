# Toying with v8
![mighty-v8](https://i.ibb.co/5Y8yTNx/do-Not-Cite.jpg)  

## Reminder
" There are four main stages that code inside V8 passes through" :

- JavaScript Code - this is what you wrote
- Hydrogen - intermediate code representation where optimizations are applied
- Lithium - machine specific code used to generate native code
- Machine Code - this is what the computer understands

## Resources
- [Awesome Medium article about it][1] (the quote above is from it)
- [jsvu][2] : README is well documented


## Setup
- Follow the Medium article
- When setting the engine up use `jsvu`
- Do NOT select "QuickJS" engine, it's integration is currently broken (7 January 2020)
- I only selected v8-debug (non-debug version doesn't seem to support `--print-bytecode` and some fun stuff like this)
- Assuming you dutifully followed the `jsvu` README, you've updated your $PATH already, so you can just: 
- `v8-debug --print-bytecode myFile.js`
- It will display in standard output (console): from there you can [cat][3] (concatenate) into a file or whatever
- **List of [available flags][4] (may be outdated: in doubt run `v8-debug --help` )**


## Todo
- User-friendly way to display the aforementioned steps (some frontend)

[1]: https://www.mattzeunert.com/2015/08/19/viewing-assembly-code-generated-by-v8.html
[2]: https://github.com/GoogleChromeLabs/jsvu
[3]: https://unix.stackexchange.com/a/44143
[4]: https://gist.github.com/cevek/ef1c9761a67d80d642f98cc75885bf31