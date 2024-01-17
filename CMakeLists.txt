#Adding Source Files to the SOURCE_FILES Variable
list(APPEND LIB_INCLUDE_FILES "include/TXT_engine/button.h")
list(APPEND LIB_INCLUDE_FILES "include/TXT_engine/display.h")
list(APPEND LIB_INCLUDE_FILES "include/TXT_engine/screen.h")
list(APPEND LIB_INCLUDE_FILES "include/TXT_engine/sprite.h")
list(APPEND LIB_INCLUDE_FILES "include/TXT_engine/Txt_Engine.h")
list(APPEND LIB_INCLUDE_FILES "include/TXT_engine/txt_engine_elements.h")
list(APPEND LIB_INCLUDE_FILES "include/TXT_engine/miscellaneous.h")

list(APPEND LIB_SOURCE_FILES "src/button.cpp")
list(APPEND LIB_SOURCE_FILES "src/display.cpp")
list(APPEND LIB_SOURCE_FILES "src/miscellaneous.cpp")
list(APPEND LIB_SOURCE_FILES "src/screen.cpp")
list(APPEND LIB_SOURCE_FILES "src/sprite.cpp")

#Create the .lib file
add_library(TextEngine STATIC ${LIB_INCLUDE_FILES} ${LIB_SOURCE_FILES})
set_target_properties(TextEngine PROPERTIES LINKER_LANGUAGE CXX)

target_include_directories(TextEngine PUBLIC "${CMAKE_CURRENT_LIST_DIR}/include")

#Add the Arson Style.h to a Project
target_include_directories(TextEngine PUBLIC "${CMAKE_CURRENT_LIST_DIR}/Arson/include")

