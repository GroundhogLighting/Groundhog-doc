# Coding standards

This project was founded by non-programmers, which explains the lack of standards and good-practices in the code. However, I have recently started following this publicly available [Ruby Style Guide](https://github.com/bbatsov/ruby-style-guide). Also, since the beggining, the code has been documented using [Yardoc](http://yardoc.org/). Groundhog is far from having a well standardized code, but I would appreciate your contributions to be styled and documented properly.

Please keep in mind the following standards before adding features to Groundhog.

1. Document your functions and methods and code using YARDOC. You may use [THIS GUIDE](http://www.rubydoc.info/gems/yard/file/docs/GettingStarted.md#docing) for learning how to do it.
2. Please follow the [Ruby Style Guide](https://github.com/bbatsov/ruby-style-guide) for coding
3. Avoid creating methods that are already available in the [SketchUp API](http://www.sketchup.com/intl/en/developer/)
4. Avoid using system calls to create, write or delete files. Use FileUtils and other Ruby modules instead.
5. When creating scripts and calling the system, avoid using Pipes. There are machines who do not like them, crushing Groundhog.
6. When calling the system, prefer cross platform implementation of system code instead of OS specific calls. For example, **rtrace -e "179\(..."** program can sometimes be replaced by **rmtxop -c ...**
7. Keep the code simple... it is better to add more simple functions than to create a horrible big function.
8. 
