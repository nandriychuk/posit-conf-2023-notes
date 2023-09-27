## dplyr 1.1.0 Features You Can't Live Without - Speaker Davis Vaughan

-   `case_when` became much less strict about mixing data types so the code below now works. Before it would give an error.

    ```{r}
    case_when(
      x >= 10 ~ "large",
      x >= 0 ~ "small",
      x < 0 ~ NA,
    )

    ```

-   you can now write grouping inline with the `summarize` call using `.by`. `group_by` is not going away :)

    ```{r}
    races %>% 
      summarise(
        wins = sum(place==1),
        .by = c(character, track)
      ) %>% 
      slice_max(wins, n=1)
    ```

-   new joins:

    -   inequality

    -   rolling

    -   overlap

    Read more about joins here: <https://r4ds.hadley.nz/joins#sec-non-equi-joins>

-   Additional improvements to investigate:

    -   `reframe(), case_match(), consecutive_id(), pick(), arrange(.locale=) argument`

## Why You Should Add Logging To Your Code (and make it more helpful) - Speaker Daren Eiri

{log4r} package

-   allows you to add "trail markers" in your code. You can add warning and error messages for your API.

-   you can send your log files through the API directly (syslog)

## CI/CD Pipelines - Oh, the Places You'll Go! - Speaker Trevor Nederlof

Setup the CI/CD pipeline using GitHub actions

-   use {shinytest2} for continuous integration

-   deploy only if CI is successful

![](C:/Users/Andrin07/AppData/Local/RStudio/tmp/paste-1BC8CDF2.png)

## Coding Tools for Industry R&D -- Development Lessons from an Analytical Lab - Speaker Camila Saez Cabezas

Shadow your users and gather the insights:

-   who are the target users?

-   how do they generate data?

-   what are their needs and challenges?

Sketch the vision and map success:

-   what building blocks do we need?

-   how do we assemble and prioritize them?

-   what are the constraints?

Develop the recipe to test milestones:

-   which scenarios are in scope?

-   how many datasets?

-   what is our performance goal and how do we measure it?

## Quickly get your Quarto HTML theme in order - Speaker Greg Swinehart

Customizaable Quarto HTML themes:

create theme.scss file and add it to a \_quarto.yml

[GitHub - gregswinehart/conf-talk-2023](https://github.com/gregswinehart/conf-talk-2023)

## Insights in 5-D! (Using magic small-multiples layouts) - Speaker Matt Dzugan

{geofacet} - The geofacet R package provides a way to flexibly visualize data for different geographical regions by providing a ggplot2 faceting function `facet_geo()` which works just like ggplot2's built-in faceting, except that the resulting arrangement of panels follows a grid that mimics the original geographic topology as closely as possible.

[GitHub - mattdzugan/facetwarp: Arrange ggplot2 Facets Using Other Numerical Columns ✨](https://github.com/mattdzugan/facetwarp)

## Note:

Check the {dockerfiler} package
