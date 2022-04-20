cmake_minimum_required ( VERSION 3.1.0 )

project ( CYRayTracing
  VERSION 3.0.0
  LANGUAGES CXX
)

# Set to c++11
set ( CMAKE_CXX_STANDARD 11 )

include_directories(src/)
set ( SOURCE_ONE_WEEKEND src/main.cc )

add_executable(ray ${SOURCE_ONE_WEEKEND})

add_custom_target(run
    COMMAND ./ray > image.ppm
    WORKING_DIRECTORY ${CMAKE_PROJECT_DIR}
)