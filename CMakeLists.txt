cmake_minimum_required (VERSION 3.21)

project (test
  LANGUAGES C Fortran
  )

list(APPEND CMAKE_MODULE_PATH "${CMAKE_CURRENT_LIST_DIR}/cmake")
if(APPLE)
  set(MKL_Fortran TRUE)
endif()
find_package(MKL QUIET)
find_package(LAPACK REQUIRED)

add_executable(sgesv_example.exe sgesv_example.F90)
target_link_libraries(sgesv_example.exe LAPACK::LAPACK)

add_executable(sgemm_example.exe sgemm_example.F90)
target_link_libraries(sgemm_example.exe LAPACK::LAPACK)
