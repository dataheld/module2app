# crow

## Overview

crow is a loose collection of helpers for your shiny development.

It can help with:

- 📦 modules
- 🧪 testing
- 📖 documentation
- ... and more

crow is **opinionated on quality** ...

- Shiny apps and their modules should be proper, exported *functions in an R package*.
- *No code generation*.
  If you feel like you need to programmatically create code, you're doing it wrong.
  (I'm not talking LLMs here, but bloated boilerplates).

... but also **flexible in implementation** ...

- *No framework*.
  You use crow, crow doesn't use you.
  (It's not like [])

... and **lightweight** ...

- *~~`Imports: crow`~~*.
  crow is a time- and line-saver during development, but doesn't want to be your dependency.
  Shiny is enough.

In all of these ways, crow is also a (tiny) opposite to [rhino](https://appsilon.github.io/rhino/), [golem](https://thinkr-open.github.io/golem/) or [leprechaun](https://leprechaun.opifex.org/).


## Installation

```r
# install.packages("pak")
pak::pak("dataheld/crow")
```

crow is a *development*-time dependency; it should not be in your `DESCRIPTION`s `Imports:`.

If you want to use it in your tests, you will have to include it in `Suggests:`.

If you don't need it for tests,
but want to otherwise record that you used it for development,
consider an [extra dependency](https://pak.r-lib.org/reference/package-dependency-types.html#extra-dependencies):

```DESCRIPTION
Config/Needs/website: dataheld/crow
```
