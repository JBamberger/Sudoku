find_package(OpenCV 4 REQUIRED core)

add_library(sudoku_utils STATIC
        src/utils.cpp include/utils.h
        include/config.h
        include/mathutil.h
        include/drawutil.h
        include/ximgproc_compat.h)
target_include_directories(sudoku_utils PUBLIC
        ${OpenCV_INCLUDE_DIRS}
        include
        )
target_link_libraries(sudoku_utils PUBLIC
        ${OpenCV_LIBS}
        )