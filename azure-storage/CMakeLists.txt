# Written by Yeonggyoo Jeon

cmake_minimum_required(VERSION 3.14)
project(azure_storage_sdk_delivery_project)

set(SANDSTONE_PROJECT_VERSION_MAJOR "0")
set(SANDSTONE_PROJECT_VERSION_MINOR "1")
set(SANDSTONE_PROJECT_VERSION_PATCH "0")
set(SANDSTONE_PROJECT_VERSION "${SANDSTONE_PROJECT_VERSION_MAJOR}.${SANDSTONE_PROJECT_VERSION_MINOR}.${SANDSTONE_PROJECT_VERSION_PATCH}")

message(STATUS "SandStone Azure Storage SDK Delivery Version = ${SANDSTONE_PROJECT_VERSION}")

add_subdirectory(azure-storage-cpp/Microsoft.WindowsAzure.Storage)
add_subdirectory(modified-samples)

