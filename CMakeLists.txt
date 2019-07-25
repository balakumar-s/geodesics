cmake_minimum_required(VERSION 3.2)

project(geodesics)
add_compile_options(-std=c++11 -Wfatal-errors)
find_package(Eigen3 REQUIRED)
find_package(OpenGL REQUIRED)
find_package(GLUT REQUIRED)
include_directories( ${OPENGL_INCLUDE_DIRS}  ${GLUT_INCLUDE_DIRS} )


include_directories(${EIGEN3_INCLUDE_DIRS})
add_executable(main main.cpp Mesh.cpp MeshIO.cpp Face.cpp Edge.cpp HalfEdge.cpp Vertex.cpp)
target_link_libraries(main ${GLUT_LIBRARY} ${OPENGL_LIBRARIES})
