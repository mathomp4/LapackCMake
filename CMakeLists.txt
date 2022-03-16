cmake_minimum_required (VERSION 3.21)

project (test
  LANGUAGES Fortran
  )

find_package(LAPACK)

add_executable(sgesv_example.exe sgesv_example.F90)
target_link_libraries(sgesv_example.exe LAPACK::LAPACK)

add_executable(sgemm_example.exe sgemm_example.F90)
target_link_libraries(sgemm_example.exe LAPACK::LAPACK)
