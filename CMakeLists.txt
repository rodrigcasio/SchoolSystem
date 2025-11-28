# min version of cmake
cmake_minimum_required(VERSION 3.10)

# name of project
project(SchoolSystem VERSION 1.0)

add_executable(SchoolSystem src/mainReviewAbstraction.cpp)
target_include_directories(SchoolSystem PUBLIC include)
