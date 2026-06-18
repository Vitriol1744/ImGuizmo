cmake_minimum_required(VERSION 3.27)
project(ImGuizmo)

set(CMAKE_CXX_STANDARD 23)
set(CXX_STANDARD_REQUIRED ON)

set (SOURCES
  src/GraphEditor.cpp
  src/ImCurveEdit.cpp
  src/ImGradient.cpp
  src/ImGuizmo.cpp
  src/ImSequencer.cpp
  src/ImVectorEditor.cpp
)

add_library(${PROJECT_NAME} ${SOURCES})
target_include_directories (${PROJECT_NAME} PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/src)
target_link_libraries (${PROJECT_NAME} PUBLIC imgui)
