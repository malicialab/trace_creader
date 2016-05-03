# trace_creader
C code to parse execution traces produced by TFD
Build
=====

1. Install CMake tool
   $ sudo apt-get install cmake

2. Configure and compile this project
   $ mkdir build
   $ cd build
   $ cmake ..
   $ make

3. Build basic documentation
   $ sudo apt-get install doxygen
   $ cd ../libtracereader
   $ doxygen -g doxygen.conf
   $ doxygen doxygen.conf
   $ firefox ./html/index.html

trace_creader usage examples
============================
*Create a trace index (for random access)
   $ ./trace_creader -trace <trace_file> -createindex
   (creates a <trace_file>.idx file)

*Display basic trace information:
   $ ./trace_creader -trace <trace_file> -header

*Display process and module information:
   $ ./trace_creader -trace <trace_file> -header -v

*Read a trace and dump it in "human-readable" format into output file:
   $ ./trace_creader -trace <trace_file> -out <output_file>

*Read a trace and dump it in "human-readable" format into output file
  including counter and verbose information
   $ ./trace_creader -trace <trace_file> -out <output_file> -count -v

*Dump the range of instructions [5,20] in the trace in "human-readable" format
   $ ./trace_creader -trace <trace_file> -out <output_file> -first 5 -last 20

