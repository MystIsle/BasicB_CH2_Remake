cmake_minimum_required(VERSION 3.20)
project(MyProject)

set(CMAKE_CXX_STANDARD 20)

# [수정됨] RECURSE를 제거하여 현재 폴더의 파일만 찾도록 변경
# 이렇게 하면 하위 폴더인 cmake-build-debug를 뒤지지 않습니다.
file(GLOB SOURCES "*.cpp" "*.h")

add_executable(MyProject ${SOURCES})