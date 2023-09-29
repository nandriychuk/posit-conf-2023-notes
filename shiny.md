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

## **From Concept to Impact: Building and Launching Shiny Apps in the Workplace [TALK-1074] - Tiger Tang,** CARFAX

Find an idea:

-   Create something that everyone can use in the company

-   Replace reoccurring work processes for a department

-   Solve challenges in a few teams

Find investors for your shiny app idea/project:

-   Don't pitch the shiny app; pitch the impact.

Build a product:

-   minimize "nice to have" widget; focus on core functionality

-   manage new feature requests

Involve users/customers for your app:

-   set-up a landing page to host all shiny apps you build if you have a few shiny apps connected by the same purpose

-   bring personality to the app

Operations:

-   make sure the app is user-friendly

-   on-boarding for new users

-   connect with stakeholders

## Shiny New Tools for Scaling your Shiny Apps [TALK-1088] - Joe Kirincic, Medical Mutual of Ohio

Potential solutions for scaling your shiny app:

-   Caching (e.g. shiny::renderChachedPlot)

-   Async operations (e.g. using {future} and {promises})

OR

-   Using JS!

The big idea is that we can scale our shiny app by shifting work from R to the browser. R is going to take the dataset that is going to be plotted and R is going to "kick-out" this dataset to every connecting browser (every connected user in a session). And from there the browser is going to be responsible from regenerating the plot when the input/dropdown updates.

To implement this, you need

-   a data manipulation library

    -   DuckDB is designed for analytics workloads and works great with shiny

    -   WASM. Assembly tailored made for the browser

        Both of these tools provide fast response for querries

-   a data visualization library

    -   observable plots. This framework is like {ggplot2} but for JS.

Caveats:

-   Browsers are not servers

-   sensitive data should not be sent to the browser

-   minor hackery needed

## The Road to Easier Shiny App Deployments [TALK-1089] - Liam Kalita,  Jumping Rivers Ltd

If your shiny app is not working on connect or wasn't deployed correctly:

-   Check the deployment log

Things to look out for:

-   hardcoded secrets

-   availability of external resources

System dependencies that you ned to consider when deploying your code:

-   C/C++ Development Tools

-   System utilities

-   TeX/LzTex

-   Quarto

Proactive approaches:

-   CI/CD

-   Containerisation (Docker)

-   Monitoring and Allerting
