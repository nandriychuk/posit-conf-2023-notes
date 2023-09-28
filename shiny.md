## Building a Flexible, Scaleable Self-Serve Reporting System with Shiny [TALK-1075] - Natalie O'Shea, BetterUp

The betterupinsights is a shiny app that pulls data from the database when the "load data" button is clicked. User can explore the data and once happy with the result the data/charts/tables get into the Google slides templates.

The architecture of the app:

-   {Rhino} for modularizing the app

-   {R6} + gargoyle triggers (Read more here: [Jiwan Heo \| Pass around data between Shiny modules with R6 (rbind.io)](https://jiwanheo.rbind.io/post/2022-02-06-pass-around-data-between-shiny-modules-with-r6/#:~:text=To%20use%20R6%20in%20your,it%20updates%20r6%27s%20name%20field.))

-   googleapi via {reticulate} to integrate previous work done in python

Natalie's advice:

-   Identify the core capability. What capability can you provide that is not already present in existing tools?

-   Create a data product. Dashboards answer questions. data products perform a valuable service. Data products must be built with maintainability and robusticity in mind ([Science as Amateur Software Development - YouTube](https://www.youtube.com/watch?v=zwRdO9_GGhY)).

-   Measure impact. Baseline ROI analysis, usage tracking, user feedback.
