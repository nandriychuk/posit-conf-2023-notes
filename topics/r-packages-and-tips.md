## dbtplyr: Bringing Column-Name Contracts from R to dbt [TALK-1098] - Emily Rieder, Capital one

Emily's package {dbtplyr}

Column names can be sentences, not just words.

1.  Define simple stubs

    stub = semantics + contracts

    (what? how?) + (who? where ?) + (why?)

2.  Explain complex concepts

    column name = (type 1 stub)\_(type_2\_stub)\_...

    e.g. ID_USER, ATM_SESSION_DURATION

## Adding a Touch of glitr: Developing a Package of Themes on Top of ggplot [TALK-1103] Aaron Chafetz, ,Karishma Srikanth, US Agency for International Development

Problem: repeating ggplot theme elements across the same file; repeating hex colors that are not standard across the file; repeating standard exports size and dpi.

Identified repetitive patterns to create a {[glitr](https://github.com/USAID-OHA-SI/glitr)} package.

Note: [ggplo docs:](https://ggplot2.tidyverse.org/reference/theme_get.html#:~:text=Thus%20this%20operator%20can%20be,to%20overwrite%20an%20entire%20theme). `+` and `%+replace%` can be used to modify elements in ggplot themes. `%+replace%` replaces the entire element; any element of a theme not specified in e2 (code after replace) will not be present in the resulting theme (i.e. NULL). Thus this operator can be used to overwrite an entire theme.

[{grDevices}](https://r-universe.dev/manuals/grDevices.html) - package to support plot's colors and fonts.

{extrafont}

The resources above were used to create {[glitr](https://github.com/USAID-OHA-SI/glitr)} so that their colleagues could them use the theme created for internal plots to standardize them with `p + si_style()`

Color:

-   check out Viz Pallete, Paletable resources;

-   Lisa Charlotte Muth: <https://lisacharlottemuth.com/2016/04/22/Colors-for-DataVis/>

## In-Process Analytical Data Management with DuckDB [TALK-1099] - Hannes Mühleisen, DuckDB Labs

Advantages of DuckDB:

-   It is an in-process (linked to the process you are in, for example R, without external setup) analytical data management system. DDB runs in the same process that R interpreter itself.

-   It supports complex SQL queries, has no external dependencies, and is deeply integrated into the R ecosystem. For example, DuckDB can run SQL queries directly on R data frames without any data transfer.

-   It is fast. It uses query processing techniques like vectorized execution and automatic parallelism.

-   It is free and open source software under the MIT license.

    Demo code: <https://gist.github.com/hannes/0c1e9c10a6a96500b4d61c8589d6c42b>

## HTML and CSS for R Users [TALK-1105] - Albert Rapp

[John Burn-Murdoch](https://twitter.com/jburnmurdoch?ref_src=twsrc%5Egoogle%7Ctwcamp%5Eserp%7Ctwgr%5Eauthor) creates great visualizations.

for CSS in {gt} you can specify the CSS code in the `opt_css(css=…))` code within R script.

for Quarto, use my_style.scss files to link your style sheet in .qmd

Albert's tutorial on youtube: <https://www.youtube.com/watch?v=QU8wSya-Y9E>

## It's a Great Time to be an R Package Developer! [TALK-1132] - Jenny Bryan/Hadley Wickham, Posit, PBC

New [R Packages (2e) (r-pkgs.org)](https://r-pkgs.org/)!

-   `use_pkgdown_github_pages()` calls pkgdown website every time your website changes and is going to create a github pages website

-   `use_github_actions()` simplifies the workflow for adding GitHub actions checks

-   updated guidance on testing, folder and file structure.

-   `use_lifecycle()`

-   `use_release_issue()`

## epoxy: Super Glue for Data-driven Reports and Shiny Apps [TALK-1155] - Garrick Aden-Buie, Posit, PBC

{epoxy} is a new package that uses {glue} to give authors templating superpowers. Epoxy works in R Markdown and Quarto, in markdown, LaTeX, and HTML outputs. It also provides easy templating for Shiny apps for dynamic data-driven reporting.

-   inline syntax

-   reusable templates

-   you can use epoxy in scripts, reports, apps (slightly different syntax for shiny) by using the epoxy chunk code like you'd use R chunk:

<!-- -->

-   build on {glue}

    -   glue is build for developers, lightweight and has no dependencies, works great in R scripts primarily

-   epoxy has inline transformers for:

    -   numbers: .dollar, .percent, .coma, .ordinal

    -   text: .titlecase, .bold, .italic

    -   you can also create your function and refer to it in the epoxy in inline code to do the calculation on the fly

    -   you can nest formatters `{.dollar {.cpm max_cost}}` where `.cpm`refers to your function

    -   epoxy can use the dataframe in the chunk or the first (or whatever other) row from data with .data = dat_name[1, ]

    -   `epoxy(), epoxy_html(). epoxy_latex(), epoxy_use_file()`

## Becoming an R Package Author (or How I Got Rich\* Responding to GitHub Issues) [TALK-1133] - Matt Herman, The Council of State Governments Justice Center

Check out {tidycensus} package.

Zed Shaw "Advice from an old programmer"

Ways to become a contributor (using GitHub):

-   Start with answering questions

-   Fix a small bug

-   Think of the small feature you'd like to be implemented

-   Use your domain knowledge to contribute
