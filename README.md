# apex_rowclick
apex_rowclick is a small dynamic action designed to reside on the global page as an "on-load" dynamic action.
# Downloading the plugin
You can download the plugin on the [demo site](https://apex.oracle.com/pls/apex/f?p=43484:210 "Demo site on apex.oracle.com")
# Using the plugin
1. Import the plug-in
2. Add an "onload" dynamic action to the page where you want to have the behaviour (this could be page 0)
3. Choose the plug-in
4. The region that should have the rowclick behavior now needs some attributes
   (be aware not to put this on the attributes or class of the grid, but to the region itself.
  1. rowclick="COLUMN_HEADER"
  2. rowclick-exclude="HEADER1,HEADER2"

In this example:

  1. rowclick adds the behavior and tells apex in what column to find the link
  2. rowclick-exclude is a comma-separated list holding all the column headers that should not have the bahavior. Often because they have a link themselves (ie a delete-link)

#Where to find / set the reference for the columns?
This depends on the type of report:
- Classic reports: the column-header is derived from the column-name in your query
- Interactive reports: the column has an "ID" attribute. Here you can set the header value and use it in your region-attributes.
