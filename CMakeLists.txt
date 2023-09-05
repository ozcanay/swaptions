cmake_minimum_required(VERSION 3.12)
project(swaptions)

set(CMAKE_CXX_STANDARD 23)

add_executable(${PROJECT_NAME} CumNormalInv.cpp  nr_routines.cpp HJM.h HJM_Securities.h HJM_Swaption_Blocking.cpp MaxFunction.cpp nr_routines.h 
resource.h HJM.cpp main.cpp HJM_SimPath_Forward_Blocking.cpp HJM_type.h RanUnif.cpp)

target_link_libraries(${PROJECT_NAME} pthread)
target_compile_definitions(${PROJECT_NAME} PUBLIC SPDLOG_ACTIVE_LEVEL=SPDLOG_LEVEL_TRACE)

