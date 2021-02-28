cmake_minimum_required(VERSION 3.15)
project(asyncpp)

foreach(APP
        each
        filter
        map
        ntimes
        sequencer
        series
        series-boost-asio
    )
  add_executable(${APP} examples/${APP}.cpp)
  #target_link_libraries(${APP} ${CONAN_LIBS} stdc++fs)
  #target_compile_definitions(${APP} PUBLIC BOOST_ASIO_DISABLE_EPOLL)
  target_compile_features(${APP} PUBLIC cxx_std_17)
endforeach()