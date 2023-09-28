## Reproducible Manuscripts with Quarto [TALK-1070] - Mine Cetinkaya-Rundel, Posit, PBC

New project type: manuscript (quarto 1.4+)

-   produce manuscripts in multiple formats

-   publish computations

    You can collaborate in the rendered output (e.g., highlight the text and add comments!)

-   you are able to embed the outputs from other notebooks (.qmd, .ipyb) in your .qmd manuscript file

## What's New in Quarto?\* [TALK-1072] - Charlotte Wickam, Posit, PBC

Note, some features described are available with version 1.4. use `quarto --version` in the CLI to view the version of quarto you are using.

Content:

-   embed outputs from other documents with one line of code `{{< embed source.qmd#fig-scatter >}}` where `#fig-scatter` is a cell identifier.

-   cross reference anything with `@fig-scatter` identifier for the div

-   inline execution for jupyter pytoncode

-   add context to code (the code file name, code annothation)

Projects:

-   run `quarto create` in the terminal to produce quarto project. Follow the prompts.

-   generate variations with project profiles using the quarto config file

Tools:

-   visual studio code extension

## **Dynamic Interactions: Empowering Educators and Researchers with Interactive Quarto Documents Using webR\* [TALK-1073] - James Balamuta,** University of Illinois Urbana-Champaign

Quarto unifies and extends the R Markdown ecosystem and allows you to switch formats without hassle.

WebAssembly allows you to run applications "in-browser" at near native speed so R runs on the web server instead of the compute server

quarto-webr extension allows you to run/rerun the code in browser.

To start using web-r in quarto:

-   Navigate to Terminal and run `quarto add coatless/quarto-webr` to install the extension

-   add `engine: knitr` to your yaml doc

-   add `filters: -webr`

-   set the code cell type to `{webr-r}` instead of `{r}`

-   you are ready to render the doc1

    you can customize the extension, look up the documentation
