cmake_minimum_required(VERSION 3.6)

set(HEADER_FILES
        QtAwesome/QtAwesome.h
        QtAwesome/QtAwesomeAnim.h)

set(SOURCE_FILES
        QtAwesome/QtAwesome.qrc
        QtAwesome/QtAwesome.cpp
        QtAwesome/QtAwesomeAnim.cpp)

set(CMAKE_INCLUDE_CURRENT_DIR ON)
set(CMAKE_AUTORCC ON)
find_package(Qt5 REQUIRED Core Gui Widgets)

add_library(QtAwesome STATIC ${HEADER_FILES} ${SOURCE_FILES})
target_link_libraries(QtAwesome Qt5::Core Qt5::Gui Qt5::Widgets)