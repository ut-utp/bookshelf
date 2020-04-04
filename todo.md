list of things to do for mdbook:
  - mermaid plugin
  - link check plugin

  - build the deps and pass them into mdbook when running mdbook test

  - add an LC-3 syntax highlight.js configuration (another repo, perhaps... or just inline it in the JS file that we're making below)

  - add support for utp-lc3 blocks (i.e. `rust,utp-lc3,editable`):
    + preprocessor:
      * strips out lines that start with # (i.e. the Rust code)
      * drops the rust part; leaves utp-lc3

    + a script that gets loaded that puts in the button that opens up the program in the web tui (use playpen_text)
    + have the same script go and:
      * register a plugin with highlight.js
      * call `hljs.highlightBlock(block)` for all the utp-lc3 blocks

    + because pre-processors aren't run for `mdbook test` we don't need a special backend; mdbook test will build out tests just fine

  - extra!!
    * get ACE to syntax highlight LC-3 right
    * one editable ASM thing somewhere in the book that let's people run arbitary lc-3 programs (outputs shown in the console, no inputs)
