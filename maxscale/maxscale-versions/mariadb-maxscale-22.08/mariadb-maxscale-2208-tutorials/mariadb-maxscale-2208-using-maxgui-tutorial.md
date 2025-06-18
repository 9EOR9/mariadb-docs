
# Using MaxGUI Tutorial

# Using MaxGUI Tutorial




* [Using MaxGUI Tutorial](#using-maxgui-tutorial)
* [Introduction](#introduction)
* [Dashboard](#dashboard)

  * [Annotation](#annotation)
  * [Create a new MaxScale object](#create-a-new-maxscale-object)
  * [View Replication Status](#view-replication-status)
* [Detail](#detail)

  * [Annotation](#annotation_1)
* [Visualization](#visualization)

  * [Configuration](#configuration)

    * [Annotation](#annotation_2)
  * [Clusters](#clusters)

    * [Annotation](#annotation_3)
* [Settings](#settings)

  * [Annotation](#annotation_4)
* [Logs Archive](#logs-archive)

  * [Annotation](#annotation_5)
* [Query Editor](#query-editor)

  * [Annotation](#annotation_6)
* [How to kill a session](#how-to-kill-a-session)

  * [Annotation](#annotation_7)




# Introduction


This tutorial is an overview of what the MaxGUI offers as an alternative
solution to [MaxCtrl](../mariadb-maxscale-2208-reference/mariadb-maxscale-2208-maxctrl.md).


# Dashboard


![](../../../.gitbook/assets/mariadb-corporation/MaxScale/22.08.17/Documentation/Tutorials/images/MaxGUI-dashboard.png.png)


## Annotation


1. [MaxScale object](https://mariadb.com/kb/en/maxscale-2208-getting-started-mariadb-maxscale-configuration-guide/#objects). i.e.
 Service, Server, Monitor, Filter, and Listener (Clicking on it will navigate
 to its detail page)
1. Create a new MaxScale object.
1. Dashboard Tab Navigation.
1. Search Input. This can be used as a quick way to search for a keyword in
 tables.
1. Dashboard graphs. Refresh interval is 10 seconds.

  * SESSIONS graph illustrates the total number of current sessions.
  * CONNECTIONS graph shows servers current connections.
  * LOAD graph shows the last second load of thread.
1. Logout of the app.
1. Sidebar navigation menu. Access to the following pages: Dashboard,
 Visualization, Settings, Logs Archive, Query Editor


## Create a new MaxScale object


Clicking on the *Create New* button (Annotation 2) to open a dialog for creating
a new object.


## View Replication Status


The replication status of a server monitored by
[MariaDB-Monitor](../mariadb-maxscale-2208-monitors/mariadb-maxscale-2208-mariadb-monitor.md) can be viewed by mousing over
the server name. A tooltip will be displayed with the following information:
replication_state, seconds_behind_master, slave_io_running, slave_sql_running.


# Detail


This page shows information on each MaxScale object and allow to edit its
parameter, relationships and perform other manipulation operations. Most of the
control buttons will be shown on the mouseover event. Below is a screenshot of a
Monitor Detail page, other Detail pages also have a similar layout structure so
this is used for illustration purpose.


![](../../../.gitbook/assets/mariadb-corporation/MaxScale/22.08.17/Documentation/Tutorials/images/MaxGUI-detail.png.png)


## Annotation


1. Settings option. Clicking on the gear icon will show icons allowing to do
 different operations depending on the type of the Detail page.

  * Monitor Detail page, there are icons to Stop, Start, and Destroy monitor.
  * Service Detail page, there are icons to Stop, Start, and Destroy service.
  * Server Detail page, there are icons to Set maintenance mode, Clear server
 state, Drain and Delete server.
  * Filter and Listener Detail page, there is a delete icon to delete the
 object.
1. Switchover button. This button is shown on the mouseover event allowing to
 swap the running primary server with a designated secondary server.
1. Edit parameters button. This button is shown on the mouseover event allowing
 to edit the MaxScale object's parameter. Clicking on it will enable editable
 mode on the table. After finishing editing the parameters, simply click the
 Done Editing button.
1. A Detail page has tables showing "Relationship" between other MaxScale
 object. This "unlink" icon is shown on the mouseover event allowing to
 remove the relationship between two objects.
1. This button is used to link other MaxScale objects to the relationship.


# Visualization


This page visualizes MaxScale configuration and clusters.


## Configuration


This page visualizes MaxScale configuration as shown in the figure below.


![](../../../.gitbook/assets/mariadb-corporation/MaxScale/22.08.17/Documentation/Tutorials/images/MaxGUI-config-visualization.png.png)


### Annotation


1. A MaxScale object (a node graph). The position of the node in the graph can
 be changed by dragging and dropping it.
1. Anchor link. The detail page of each MaxScale object can be accessed by
 clicking on the name of the node.
1. Filter visualization button. By default, if the number of filters used by a
 service is larger than 3, filter nodes aren't visualized as shown in the
 figure. Clicking this button will visualize them.
1. Hide filter visualization button.
1. Refresh rate dropdown. The frequency with which the data is refreshed.
1. Create a new MaxScale object button.


## Clusters


This page shows all monitor clusters using
[mariadbmon](../mariadb-maxscale-2208-monitors/mariadb-maxscale-2208-mariadb-monitor.md) module in a card-like view.
Clicking on the card will visualize the cluster into a tree graph as shown in
the figure below.


![](../../../.gitbook/assets/mariadb-corporation/MaxScale/22.08.17/Documentation/Tutorials/images/MaxGUI-cluster-visualization.png.png)


### Annotation


1. Drag a secondary server on top of a primary server to promote the secondary
 server as the new primary server.
1. Server manipulation operations button. Showing a dropdown with the following
 operations:

  * Set maintenance mode: Setting a server to a maintenance mode.
  * Clear server state: Clear current server state.
  * Drain server: Drain the server of connections.
1. Quick access to query editor button. Opening the `Query Editor` page for
 this server. If the connection is already created for that server, it'll use
 it. Otherwise, it creates a blank worksheet and shows a connection dialog to
 connect to that server.
1. Carousel navigation button. Viewing more information about the server in the
 next slide.
1. Collapse the carousel.
1. Anchor link of the server. Opening the detail page of the server in a new
 tab.
1. Collapse its children nodes.
1. Rejoin node. When the `auto_rejoin` parameter is disabled, the node can be
 manually rejoined by dragging it on top of the primary server.
1. Monitor manipulation operations button. Showing a dropdown with the
 following operations:

  * Stop monitor.
  * Start monitor.
  * Reset Replication.
  * Release Locks.
  * Master failover. Manually performing a master failover. This option is
 visible only when the `auto_failover` parameter is disabled.
1. Refresh rate dropdown. The frequency with which the data is refreshed.
1. Create a new MaxScale object button.


# Settings


This page shows and allows editing of MaxScale parameters.


![](../../../.gitbook/assets/mariadb-corporation/MaxScale/22.08.17/Documentation/Tutorials/images/MaxGUI-settings.png.png)


## Annotation


1. Edit parameters button. This button is shown on the mouseover event allowing
 to edit the MaxScale parameter. Clicking on it will enable editable mode on
 the table..
1. Editable parameters are visible as it's illustrated in the screenshot.
1. After finishing editing the parameters, simply click the Done Editing
 button.


# Logs Archive


This page show real-time MaxScale logs with filter options.


![](../../../.gitbook/assets/mariadb-corporation/MaxScale/22.08.17/Documentation/Tutorials/images/MaxGUI-logs-archive.png.png)


## Annotation


1. Filter by dropdown. All logs types are selected to be shown by default
1. Uncheck the box to disable showing a particular log type.


# Query Editor


A SQL editor tool to run queries and perform other SQL operations.


![](../../../.gitbook/assets/mariadb-corporation/MaxScale/22.08.17/Documentation/Tutorials/images/MaxGUI-query-editor.png.png)


## Annotation


1. Worksheet tab navigation. Each worksheet is bound to a connection, so
 sessions querying within a worksheet is not yet supported.
1. Add a new worksheet button.
1. Connection manager dropdown. With this dropdown, you can create a new
 connection or change the connection for the current active worksheet. A new
 connection can be created by selecting the last option in the dropdown
 labeled as `New connection`. Once a connection is created, it automatically
 binds the connection to the current active worksheet.
1. Active database dropdown. Right-click on the database name and click
 `Use database` option to quickly change the default (current) database
1. Schemas sidebar. Showing available schemas on the current connection. As
 shown in the figure above, these items can be explored to show tables,
 stored procedures, columns, and triggers within the schema.
1. Schemas sidebar object.

  * Each object has its own context menu providing different options. e.g. For
 the table object as shown in the figure above, it has options to
 `Preview Data (top 1000)` and `View Details`. The query result for these
 options is shown in the `Data Preview` result tab which is annotated as
 number 12. The context menu can be shown by right-clicking on the object
 or clicking on the three dots icon placed on the right side of the object.
  * Quick access to the `Preview Data (top 1000)` context menu option. For a
 table object, its preview data can also be seen by clicking on its name.
  * Quick overview tooltip. Each object has its own tooltip providing an
 overview of the object.
1. Refresh schema objects button. After deleting or creating schema object, the
 `Schemas sidebar` needs to be manually refreshed.
1. Collapse the `Schemas sidebar` button.
1. SQL editor. The editor is powered by
 [Monaco editor](https://microsoft.github.io/monaco-editor/) which means its
 functionalities are similar to VS code. Available commands can be seen by
 pressing F1 while the cursor is active on the editor. This is an intention
 to prevent conflict between the browser's shortcut keys and the SQL
 editor's. This also means the editor shortcut key commands are valid only
 when the cursor is active on the `SQL editor` with an exception for the
 `Run all statements`, `Run selected statements` and
 `Save statements to favorite` commands.
1. Query Results. Showing the query results of queries written in the SQL
 editor.
1. Data Preview. Showing the query results of `Preview Data (top 1000)` and
 `View Details` options of the schema sidebar context menu.
1. History/Snippets. Showing query history and snippet queries.
1. Result tab navigation. Navigating between SQL queries results.
1. Filter query history logs. The query history is divided into two types of
 logs The `User query logs` contains logs for queries written in the
 `SQL editor` while the `Action logs` contains logs for auto-generated SQL,
 such as `Preview Data (top 1000)`, `View Details`, `Drop Table` and
 `Truncate Table`.
1. Export query result button. Exporting as `json`, `csv` with a custom
 delimiter.
1. Filter query result columns dropdown. Selecting columns to be visible.
1. Vertical query result button. Switching to vertical mode.
1. Run button. Running the queries written in the `SQL editor`. Alternatively,
 pressing `Ctrl/CMD+Shift+Enter` to `Run all statements` or `Ctrl/CMD+Enter`
 to `Run selected statements`.
1. Visualize query result button. Visualizing a query result into a line,
 scatter, vertical bar, and horizontal bar graph.
1. Create a query snippet from the queries written in the `SQL editor`.
 Alternatively, press `Ctrl/CMD+D`.
1. Open Script button.
1. Save Script button. This writes content into the opened file. This only
 works on Chrome or any browsers based on Chromium served over a secure
 connection (https)
1. Save Script As button. Save the content as a new file.
1. [sql_select_limit](https://mariadb.com/docs/reference/mdb/system-variables/sql_select_limit/)
 input. Changing the maximum number of rows to return from SELECT statements.
1. Add a new session button.
1. Query Editor settings button. Open `Query configuration` dialog to change
 the value of `Max rows` (sql_select_limit),
 `Query history retention period (in days)`,
 `Show confirmation before executing the statements` and
 `Show system schemas`.
1. Maximize Query Editor window.


# How to kill a session


A session can be killed easily on the "Current Sessions" table which can be
found on the [Dashboard](#dashboard), Server detail, and Service detail page.


![](../../../.gitbook/assets/mariadb-corporation/MaxScale/22.08.17/Documentation/Tutorials/images/MaxGUI-kill-session.png.png)


## Annotation


1. Kill session button. This button is shown on the mouseover event.
1. Confirm killing the session dialog.


CC BY-SA / Gnu FDL

