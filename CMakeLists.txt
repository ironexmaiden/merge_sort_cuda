cmake_minimum_required(VERSION 3.10)
project (cuda_sort)
enable_language(CUDA)
find_package(CUDA)

add_executable(cuda_sort cuMergesort.cu cuMergesort.h checker.c)
target_link_libraries(cuda_sort ${CUDA_LIBRARIES})
message(${CUDA_LIBRARIES})
