# RinsideExample2

Rinside example 2.

## CppRinsideExample2.pro

```

include(../../ConsoleApplication.pri)
include(../../Libraries/Rinside.pri)

SOURCES = \
  main.cpp
```

## main.cpp

```c++
#pragma GCC diagnostic push
#pragma GCC diagnostic ignored "-Weffc++"
#pragma GCC diagnostic ignored "-Wunused-local-typedefs"
#pragma GCC diagnostic ignored "-Wunused-but-set-parameter"
#pragma GCC diagnostic ignored "-Wextra"
#include <RInside.h>
#pragma GCC diagnostic pop

int main(int argc, char *argv[])
{
  RInside R(argc, argv);
  R["txt"] = "Hello World\n";
  R.parseEvalQ("cat(txt)");
}
```