
#conan_cmake_run(REQUIRES

                # Libraries to be installed locally
                #                gtest/1.8.1@bincrafters/stable

                #                BASIC_SETUP
                #                BUILD missing
                #                )

#========== Find Packages =====================#
find_package(GTest REQUIRED)
include(GoogleTest)

add_executable(tests constexpr_test.cpp)
target_link_libraries(tests GTest::GTest GTest::Main -lpthread)
gtest_discover_tests(tests)
