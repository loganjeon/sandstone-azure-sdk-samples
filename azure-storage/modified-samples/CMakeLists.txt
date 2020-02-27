# Written by Yeonggyoo Jeon

set(AZURESTORAGE_INCLUDE_DIR ${CMAKE_SOURCE_DIR}/azure-storage-cpp/Microsoft.WindowsAzure.Storage/includes)
set(AZURESTORAGE_INCLUDE_DIRS ${CMAKE_SOURCE_DIR}/azure-storage-cpp/Microsoft.WindowsAzure.Storage/includes ${CASABLANCA_INCLUDE_DIR} ${Boost_INCLUDE_DIRS} ${OPENSSL_INCLUDE_DIRS} ${UUID_INCLUDE_DIRS} ${LibXML2_INCLUDE_DIR})

set(AZUREAZURAGE_LIBRARY_SAMPLE azurestoragesample)

add_subdirectory(samples)
