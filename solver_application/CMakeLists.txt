cmake_minimum_required(VERSION 3.4)
project(solver)
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
add_subdirectory(/home/matvey/formatter_ex_lib formatter_ex_lib_dir)
add_subdirectory(/home/matvey/solver_lib solver_lib_dir)
add_executable(solver /home/matvey/solver_application/equation.cpp)

target_include_directories(solver PUBLIC
/home/matvey/formatter_ex_lib
/home/matvey/solver_lib
)
target_link_libraries(solver formatter_ex_lib solver_lib)

