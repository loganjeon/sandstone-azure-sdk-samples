# Written by Yeonggyoo Jeon

cmake_minimum_required(VERSION 3.14)
project(azure_iothub_sdk_delivery_project)

set(SANDSTONE_PROJECT_VERSION_MAJOR "0")
set(SANDSTONE_PROJECT_VERSION_MINOR "1")
set(SANDSTONE_PROJECT_VERSION_PATCH "0")
set(SANDSTONE_PROJECT_VERSION "${SANDSTONE_PROJECT_VERSION_MAJOR}.${SANDSTONE_PROJECT_VERSION_MINOR}.${SANDSTONE_PROJECT_VERSION_PATCH}")

message(STATUS "SandStone Azure Iothub SDK Delivery Version = ${SANDSTONE_PROJECT_VERSION}")

add_subdirectory(azure-iot-sdk-c)
add_subdirectory(modified-samples)
