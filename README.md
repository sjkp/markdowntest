# markdowntest

In addition to the usual extension UI elements, such as browser actions, context menus and popups, a DevTools extension can add UI elements to the DevTools window:

A panel is a top-level tab, like the Elements, Sources, and Network panels.
A sidebar pane presents supplementary UI related to a panel. The Styles, Computed Styles, and Event Listeners panes on the Elements panel are examples of sidebar panes. (Note that the appearance of sidebar panes may not match the image, depending on the version of Chrome you're using, and where the DevTools window is docked.)

![image](https://user-images.githubusercontent.com/3397744/138170531-621cb809-4c94-4b91-ae82-3b9feb714274.png)


DevTools window showing Elements panel and Styles sidebar pane.
Each panel is its own HTML file, which can include other resources (JavaScript, CSS, images, and so on). Creating a basic panel looks like this:
```
chrome.devtools.panels.create("My Panel",
    "MyPanelIcon.png",
    "Panel.html",
    function(panel) {
      // code invoked on panel creation
    }
);
```
