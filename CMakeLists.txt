cmake_minimum_required(VERSION 3.1.0)

project(qmarkdown)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED TRUE)

set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)

find_package(Qt5Core REQUIRED)
find_package(Qt5Widgets REQUIRED)
find_package(Qt5WebEngineCore REQUIRED)
find_package(Qt5WebEngineWidgets REQUIRED)
find_package(Qt5WebChannel REQUIRED)
find_package(Qt5Gui REQUIRED)

set(CMAKE_CXX_FLAGS "-O3 -Wall -Wextra")

add_executable(qmarkdown
    src/helpers.cpp
    src/resgen.cpp
    src/fileinput.cpp
    src/preview.cpp
    src/document.cpp
    src/mainwindow.cpp
    src/main.cpp
    src/resources/qmarkdown.qrc
)

set(CMAKE_EXPORT_COMPILE_COMMANDS TRUE)

target_link_libraries(qmarkdown Qt5::Widgets Qt5::Core Qt5::WebEngineCore
    Qt5::WebEngineWidgets Qt5::WebChannel Qt5::Gui stdc++fs)

install(TARGETS qmarkdown DESTINATION ${DESTDIR}${PREFIX}/usr/bin)
