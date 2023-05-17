Creating Starter Project:
- Once the final project is ready, create the helper files to paste the code which you will need for demonstartion in the project.

- Start with 2nd section. Here Layout widgets for me.
Steps:
1. First check the codes that is required for explaining the concept. Remove the codes.
2. if there are codes which will be used by instructor, just to make it easy/quick, but not relevant to the concept, add it to the helper file.
3. After the code is removed, add comments with TODO

- remove the dependencies which you might want to add during teaching

## Section 2: LAYOUT WIDGETS

## V1 - Container & Padding
## V2 - Row & Column
## V3 - Wrap
## V4 - FractionallySizedBox
## V5 - Expanded widget and SizedBox
## V6 - Stack

## Section 3: BASIC WIDGETS

## V1 Icon & IconButton:
## V2 - Text & Typography
## V3 Buttons
## V4 TextField
## V5 Card & Inkwell
## V6 Images
## V7 Other Stateful widgets

## Section 4: APPBAR

# V1 Overview of AppBar
# V2 Basic Appbar
# V3 BottomBar & FAB
# V4 Slivers
# V5 Search Bar:


## Section 5: LIST WIDGETS

# V1 Introduction to Lists in Flutter
# V2 GridView.count()
# V3 ListTile & ExpansionTile
# V4 ListView using builder
# V5 Dismissable Widget
# V6 Reorderable ListView
# V7 DataTable


## Section 6: Navigation Widget

# V1: Introducing Navigation Widgets
# V2: Tab
# V3 - Dialogs
# V4 - Route
# V5 - NavigationDrawer
# V6 - PageSelector
# V7 - DraggableScrollableList

## Section 7: ASYNC WIDGETS

# V1 - Understanding Async Processes
# V2 - FutureBuilder()
# V3 - StreamController & StreamBuilder


--------------======================--------------======================-------------

** references: 
https://medium.flutterdevs.com/explore-futurebuilder-in-flutter-9744203b2b8c


FutureBuilder is a widget that utilizes the result of a Future to build itself. 

- add FutureBuilder Widget
- add future property, with the desired output from a resource
- add builder
- check connection state i.e. (connectionState.done?). if it is done, return the desired output, else return the progress bar(or anythimg that you want until the resource is loaded)
- its good practice to check for an error while the future is resolving.
- explain/brief about other connection states

- In this example we first have an async operatio that takes ~3 seconds and succeeds with the content loading.
Note this is just for demonstration purposes


The dart:async library contains two types that are important for many Dart APIs: Stream and Future. Where a Future represents the result of a single computation, a stream is a sequence of results. You listen on a stream to get notified of the results (both data and errors) and of the stream shutting down. You can also pause while listening or stop listening to the stream before it is complete.

# StreamBuilder
** refereces:
https://medium.flutterdevs.com/exploring-streambuilder-in-flutter-5958381bca67
The Stream resembles a line. At the point when you enter a value from one side and a listener from the opposite side, the listener will get that value. A stream can have various listeners and that load of listeners can get the pipeline, which will get equivalent value. How you put values on the stream is by utilizing the Stream Controller. A stream builder is a widget that can change over user-defined objects into a stream.


https://www.youtube.com/watch?v=QCz8ekQi-BE


Stream controller includes he entire process which include:
- Input is called sink and output is stream.
- subscriber is StreamBuilder: the widget that uses our stream data
- KEEP adding data in the sink. Subscriber will listen to it and will be updated.
- snapshot is the data in the stream


- add FAB and all the code related to it
- add the streamBuilder widget
- define the numeric counter and StreamController.
- add builder and stream property
- in the builder, explain about the connectionState and all the other states which is checked.
- add the counter to the sink in FAB onPressed method.
    myStreamController.sink.add(counter);



** in browser - html
** in mobile - canvas kit renderer
** for web: run command
 flutter run -d chrome --web-renderer html



## Slivers: https://medium.flutterdevs.com/explore-slivers-in-flutter-d44073bffdf6
Slivers are a part of scrollabale area. It provides all the customisation you might want for creating a scrollable area.
Under the hood, scrollable items like list view and gridview use slivers .
- explain why slivers is used inside custom scroll view
CustomScrollView in Flutter is a scroll see that permits us to make different scrolling over impacts, for example, grids, lists, and extending headers. It has a sliver property where we can pass a list of widgets that incorporate SliverAppBar, SliverFixedExtentList, SliverList, and SliverGrid, and so on.
- add expanded height(the most extreme height of the application bar that can be extended while scrolling), flexispace, background
- show difference in title in flexispace and sliverBar

- add SliverFillRemaining
- add SliverFixedExtentList
    * all the children here will have the itemExtent of 150. There will be no space between the childern
- if yo uwant to add a list here, use the sliverList, sliverGrid for grid list
- add pin, float, snap, background colour
- float: make the app bar reappear when you scroll down, even if you haven’t reached the top of the list



## BottomSheet

- BottomSheet
    - explain the types of bottomSheet
        - Standard bottom sheets display supplemental content without restricting the user from interacting with the main part of the app while the sheet is visible. Standard bottom sheets are also known as persistent bottom sheets
        - Modal bottom sheets show supplemental data while restricting users from interacting with other parts of the app. The user must dismiss the modal bottom sheet to continue interacting with the app’s main content
        - Expanding bottom sheets are like a hybrid of standard and modal bottom sheets. An expanding bottom sheet enables the user to access both the standard sheet and information presented in the modal bottom sheet