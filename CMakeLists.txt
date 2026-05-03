cmake_minimum_required(VERSION 4.0.0)
project(Hello)

include(FetchContent)
FetchContent_Declare(cxxopts
  GIT_REPOSITORY https://github.com/TobiZehPanda/cpp_lib_personal
)
FetchContent_MakeAvailable(cpp_lib_personal)

add_executable(HelloApp src/main.cpp)

target_compile_features(HelloApp PUBLIC cxx_std_20)

target_link_libraries(HelloApp PRIVATE
  cpp_lib_personal
)
