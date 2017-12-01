## Learn How To Program a Shiny App
This page will be a very brief tutorial on how to make an interactive graph with **Shiny Apps**!


##### 1. Create the UI.R and server.R files
Both of these files are required to make a Shiny App.


The UI (user interface) file is required to code for the aesthetic portion of the interactive app. There are multiple features called **widgets** that can , such as buttons to select options, drop-down menus, and more.


The server file is required to code for the functional part of the shiny app: it determines how each the app behaves, rather than the aesthetic appearance of it.


Make sure to install the Shiny library to use shiny!

##### 2. Write the UI.R file

```
shinyUI(
  fluidPage(
    titlePanel(
        # Code for title of graph goes here!),

    sidebarLayout(
      sidebarPanel(
        # Code goes here! ),
      mainPanel(
        # Code goes here! )
    )
  )
)
```

##### 3. Write the server.R file

This is a basic template used to code for the behavior of the app.

```
shinyServer(
  function(input, output) {
    output$histogram <- renderPlot({
    ## Code goes HERE!  
    })
})
```
