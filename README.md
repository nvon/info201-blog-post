## Learn How To Program a Shiny App
This page will be a very brief tutorial on how to make an interactive graph with **Shiny Apps**!


##### 1. Create the UI.R and server.R files
Both of these files are required to make a Shiny App.


The UI (user interface) file is required to code for the aesthetic portion of the interactive app. There are multiple features called **widgets** that can , such as buttons to select options, drop-down menus, and more.


The server file is required to code for the functional part of the shiny app: it determines how each the app behaves, rather than the aesthetic appearance of it.


Make sure to install the Shiny library ( through: library(shiny) ) to use shiny!


##### 2. Write the UI.R file

Here's a basic template to code for the aesthetic portion of the app.

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
Everything is contained under the ShinyUI function.

**fluidPage()** allows you to create a page where page elements are neatly organized into column and rows.
<br>
The **titlePanel()** panel codes for the title you want displayed in large text at the top of the app page.
<br>
**sidebarLayout** is required to make a page layout for **sidebarPanel()**, which places a sidebar (small panel) on your page for small interactive objects such as widgets, and **mainPanel()**, which places a large panel on your page, usually for large or important page elements such as graphs and tables.


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
All shiny servers require an **input** and an **output**. The **input** is the data you usually put in (such as data from a data frame), and **output** defines how the data is manipulated and how they should be displayed on the UI.

##### 4. Add widgets to the app
The official [shiny gallery](https://shiny.rstudio.com/gallery/) contains a large number of widget examples to play around with, and the code for each widget.

Sliders are a popular widget used to change the input values of a graph. Click the link to visit the Sliders page for the UI.R file: https://shiny.rstudio.com/gallery/sliders.html

Input your parameters, place the corresponding code to control its behavior in the server.R file, and you're done!
