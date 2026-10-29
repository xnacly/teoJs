# teoJs

> High performance ECMAScript implementation targetting a "sensible" subset of ES2015

Teo is a substring in my name and it also stands for "the extremly optimised Js (runtime)" (here)

## Goals / Project scope

- be very fast
- be interesting to me
- tiered, speculative and feedback-directed method JIT
- do on stack replacement
- do deopt ofc
- do tailcalls
- do inline caches
- do parallel jit and gc
- optimising prototypes
- lower JS builtins to machine instructions where applicable (Math.sqrt)
- reuse another backend of a programming language of mine to do JITing and IR optimisations

## ES2015 Deviations:

> See [ECMAScript® 2015 Language Specification](https://ecma-international.org/wp-content/uploads/ECMA-262_6th_edition_june_2015.pdf)

- Module only
- No `eval()` or `Function`
- Prototypes are immutable after creation
- Builtin objects are immutable
- No Annex B (Additional ECMAScript Features for Web Browsers)

## Dependencies

This is mainly a research project of mine, the following dependencies are employed as follows:

- [oxc_parser](https://crates.io/crates/oxc_parser) and [oxc_ast](https://crates.io/crates/oxc_ast) for parsing and representing ECMAScript
- [purple_garden](https://github.com/xnacly/purple-garden) for JITing specialised hot functions and other things (interning, etc)
- [regress]() for ECMA regex literals and thus objects
