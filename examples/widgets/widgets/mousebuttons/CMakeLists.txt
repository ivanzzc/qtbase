# Generated from mousebuttons.pro.

cmake_minimum_required(VERSION 3.14)
project(mousebuttons LANGUAGES CXX)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_AUTOUIC ON)

set(INSTALL_EXAMPLEDIR "examples/widgets/widgets/mousebuttons")

find_package(Qt6 COMPONENTS Core)
find_package(Qt6 COMPONENTS Gui)
find_package(Qt6 COMPONENTS Widgets)

add_qt_gui_executable(mousebuttons
    buttontester.cpp buttontester.h
    main.cpp
)
target_link_libraries(mousebuttons PUBLIC
    Qt::Core
    Qt::Gui
    Qt::Widgets
)

install(TARGETS mousebuttons
    RUNTIME DESTINATION "${INSTALL_EXAMPLEDIR}"
    BUNDLE DESTINATION "${INSTALL_EXAMPLEDIR}"
    LIBRARY DESTINATION "${INSTALL_EXAMPLEDIR}"
)
