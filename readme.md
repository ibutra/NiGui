NiGui
=====

NiGui is a cross-platform, desktop GUI toolkit written in [Nim](https://nim-lang.org/).<br>
NiGui provides an easy way to develop applications in Nim with a full-featured graphical user interface.

Target platforms:
* Linux over GTK+ 3
* Windows (Win32 API)
* macOS (planned)

Design goals:
* **Full abstraction**<br>
NiGui provides full abstraction of the underlying platform. NiGui applications are written once and can be compiled for different platforms. Application developers don't have to care about platform-specific details.
* **Simple and elegant**<br>
NiGui has a clean and beginner-friendly high-level API. It is much less complex than the Win32 API, GTK+ or Qt.<br>
NiGui profits of Nim's features and elegance in contrast to C code, for example Nim's polymorphism capabilities. 
* **Powerful**<br>
NiGui uses the native controls of the underlying platform to give a familiar use and feel for the user. In addtion, NiGui allows to create custom controls for special use cases or a themed UI. <br>
NiGui has it's own layout manager for automatic resizing and positioning of controls.
* **Minimal dependencies**<br>
The NiGui source code has no dependencies except Nim's standard library. Platform bindings are included.<br>
Generated binaries (exe files) include NiGui and do not need external libraries. 

Current state
-------------
NiGui is currently work in progress. Very basic things work, many things are missing.

Working:
* Window, Button, Label, TextBox, TextArea
* LayoutContainer (own layout manager)
* Timers
* Message boxes and file dialogs
* Custom controls including scrolling
* Drawing and image processing

WIP:
* Event handling
* Documentation

Planned:
* macOS support
* More widgets

Getting started
---------------
Recommended steps to use NiGui:
1. Clone the NiGui repository
2. Add the follwing two include paths to your Nim configuration:

For Linux/Gtk:
```
--path:"<path_to_nigui>/src/common"
--path:"<path_to_nigui>/src/gtk3"
```

For Windows:
```
--path:"<path_to_nigui>/src/common"
--path:"<path_to_nigui>/src/windows"
```

To disable the command line window under Windows, add the follwing line to your Nim configuration:
```
--app:gui
```
  
3. Try the included example programs

Show cases
----------
* [NiCalc](https://github.com/trustable-code/NiCalc) - Simple calculator

Contributing
------------
You can help to improve NiGui by:
* Trying to use it and giving feedback
* Test the programs under different Windows versions or Linux distributions
* Developing show cases
* Help improving and extending the code
* Adding macOS support

Contact: simonkrauter@openmailbox.org

License
-------

NiGui is FLOSS (free and open-source software) licensed under the [MIT License](https://opensource.org/licenses/MIT). As a result you may use any compatible license (essentially any license) for your own programs developed with NiGui. You are explicitly permitted to develop commercial applications using NiGui.