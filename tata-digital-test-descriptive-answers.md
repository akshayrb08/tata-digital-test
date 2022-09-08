1. Can we nest the Scaffold widget? Why or Why not?
A -> Why not-
     UI(widget) to be assigned to body param of the Scaffold as Scaffold is a material widget.
       Else the UI would be over a darkbackground with text being in red color and have yellow scribbly
       lines due to lack of Material widget wrapped.
     Why-
     2)If the UI should occupy only the space available other than status bar
       and device navigation bar, we can wrap the Scaffold with SafeArea Widget
     3)If we need to blend the status bar color with the UI color, we can wrap Scaffold
       with AnnotatedRegion Widget which gives us the option to set the systemOverlay
    So, We can nest Scaffold, but assuring the UI widget is passed to the body param of the Scaffold


2. What are the different ways we can create a custom widget ?
A -> Create own custom class that can be reused
     1)pass the custom properties through the constructor and pass them to widget params
     2)create multiple constructors for different behaviour pass custom data to widget params
     3)Extend the widget that should be customised and override the necessary methods which
       will have the custom code


3. How can I access platform(iOS or Android) specific code from Flutter?
A -> We can access platform specific code through MethodChannel class or EventChannel Class based on requirement
    1)MethodChannel can be used for a single output scenario(upload data to server), specify name(key to be matched at native end)
    2)EventChannel can be used to get frequent updates scenario(battery/wifi data), specify name(key to be matched at native end)
    Through the invokeMethod-(takes key to be matched at native end), native code is executed


4. What is BuildContext? What is its importance?
A -> 1)BuildContext is an class which gives context(object) of the widget associated to the widget tree.
     2)BuildContext is necessary to gain access to currentState of a widget or to call function
      of the widget to update
     3)BuildContext is required for any StateManagement to work
     4)BuildContext is necessary for navigation between widgets