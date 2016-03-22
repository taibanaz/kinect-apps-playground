# Introduction #

In order to run the fingertip detection code, you will need to install libfreenect and its dependencies. This is currently tested only on OS X, but should work on any Linux machine.

# Details #

Assuming you are building on OS X -<br>
1. Download libfreenect: <a href='https://github.com/OpenKinect/libfreenect'>https://github.com/OpenKinect/libfreenect</a><br>
2. Install for OS X: <a href='http://openkinect.org/wiki/Getting_Started#OS_X'>http://openkinect.org/wiki/Getting_Started#OS_X</a>

<h1>Using Eclipse</h1>

This section describes how you can setup Eclipse Galileo to compile projects using libfreenect:<br>
- Create an Eclipse C++ project:<br>
- File -> New -> Project<br>
- C/C++ -> C++ Project<br>
- Project Type -> Executable -> Empty Project<br>
- Toolchains -> MacOSX GCC<br>
- Enter project name (e.g. "Fingertip")<br>
- Click Finish<br>
- Copy the code in kinect-apps-playground/fingertip-detect to the project directory "Fingertip".<br>
- Project -> Properties -> C/C++ Build -> Setings<br>
- Tool Settings -> MacOS X C++ Linker<br>
- Set Command to g++<br>
- Tool Settings -> MacOS X C++ Linker -> Libraries<br>
- Libraries (-l) (Add): freenect, freenect_sync (Add both separately)<br>
- Tool Settings -> MacOS X C++ Linker -> Miscellaneous<br>
- Add to Linker flags: -framework GLUT -framework OpenGL<br>
- Tool Settings -> GCC C++ Linker -> Directories<br>
- Include paths (-I) (Add): /usr/local/include/libfreenect<br>
- Right click on project "Fingertip" in project explorer -> Clean Project<br>

Run the project as a Local C/C++ Application.