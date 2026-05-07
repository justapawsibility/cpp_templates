cmake_minimum_required(VERSION 4.0.0)
project(Hello)

include(FetchContent)
FetchContent_Declare(glok
  GIT_REPOSITORY https://github.com/TobiZehPanda/grand_library_of_knowledge.git
  GIT_TAG main
)
FetchContent_MakeAvailable(glok)

add_executable(HelloApp src/main.cpp)

target_compile_features(HelloApp PUBLIC cxx_std_17)

target_link_libraries(HelloApp PRIVATE
  glok
)
