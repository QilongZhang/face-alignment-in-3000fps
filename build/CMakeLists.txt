cmake_minimum_required(VERSION 2.8)
find_package( OpenCV REQUIRED )

set(source ./../LBF.h ./../liblinear/tron.cpp ./../liblinear/tron.h ./../liblinear/linear.h ./../liblinear/linear.cpp ./../LBF.cpp ./../TrainDemo.cpp ./../TestDemo.cpp ./../facedetect.cpp ./../Utils.cpp ./../Tree.h ./../Tree.cpp ./../RandomForest.cpp ./../RandomForest.h ./../LBFRegressor.h ./../LBFRegressor.cpp)
add_executable(LBF.out ${source})
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS}")
target_link_libraries(LBF.out ${OpenCV_LIBS}  blas.a) 
