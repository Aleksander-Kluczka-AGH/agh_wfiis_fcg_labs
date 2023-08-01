# Fundamentals of computer graphics

Code written for Applied Computer Science **Fundamentals of computer graphics** course at [AGH UST](https://www.agh.edu.pl/en) [WFiIS](https://www.fis.agh.edu.pl/en/).

Semester `4`, year `2021`.

## Build with CMake:

`CMakeLists.txt` (for SFML)

```cmake
CMAKE_MINIMUM_REQUIRED(VERSION 3.19)

SET(PROGRAM_NAME GFK)
PROJECT(GFKProject)

SET(CMAKE_CXX_FLAGS "-Wall -pedantic")
SET(CMAKE_CXX_STANDARD 17)
SET(CMAKE_CXX_STANDARD_REQUIRED True)
SET(CMAKE_COLOR_MAKEFILE True)

INCLUDE_DIRECTORIES("${PROJECT_SOURCE_DIR}/include")
FILE(GLOB SOURCES "${PROJECT_SOURCE_DIR}/src/*.cpp")

SET(SFML_STATIC_LIBRARIES TRUE)
SET(SFML_DIR "#[[Your SFML Directory]]")
FIND_PACKAGE(SFML 2.5 COMPONENTS system window graphics REQUIRED)

ADD_EXECUTABLE(${PROGRAM_NAME} main.cpp ${SOURCES})
TARGET_LINK_LIBRARIES(${PROGRAM_NAME} PUBLIC sfml-system sfml-window sfml-graphics)
```

## License

Sources are licensed under MIT, a free and open-source license. For details, please see [the license file](LICENSE.md).
