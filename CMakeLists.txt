cmake_minimum_required(VERSION 2.8)
project(netalyzer)

set(NETALYZER_MAJOR_VERSION 0)
set(NETALYZER_MINOR_VERSION 1)
set(NETALYZER_PATCH_VERSION 0)
set(NETALYZER_VERSION
  ${NETALYZER_MAJOR_VERSION}.${NETALYZER_MINOR_VERSION}.${NETALYZER_PATCH_VERSION})


find_library(ZMQ libzmq.a ${PROJECT_SOURCE_DIR}/lib)


add_executable(Master master.cpp include/zmq.h include/zmq.hpp include/zmq_utils.h)




target_link_libraries(Master zmq)
