
Foreign Function Interfaces #FFI allow you to call subroutines from one language to another.


# complications

wrapper needs to be used for #guest-functions, which are implemented by a user within the language but does not come standard.

if the host language uses #garbage-collection then there exists more of a problem for a user to make sure that the FFI works as expected.

advanced or non-trivial datatypes may pose a mapping issue. having a reference to the a complicated datatype that exists

if a specific language backend exists within a #virtual-machine.

#inheritance may be a little tricky


# E.g

In C / C++ `extern C` will disable [[Name Mangling]] 