cmake_minimum_required(3.17)

project(lox-interprete
        VERSION 0.0.1
        DESCRIPTION "Interpreter for lox language from Robert Nystrom's \"Crafting Interpreters\""
        LANGUAGES CXX)

include(cmake/Sanitizers.cmake)
include(CTest)

add_subdirectory(lox-interpreter)

if(BUILD_TESTING)
  add_subdirectory(test)
  add_subdirectory(fuzz_test)
endif()