# Written by Yeonggyoo Jeon

set(DEV_AUTH_MODULES_CLIENT_INC_FOLDER "${CMAKE_SOURCE_DIR}/azure-iot-sdk-c/provisioning_client/inc" "${CMAKE_SOURCE_DIR}/azure-iot-sdk-c/provisioning/inc/internal" CACHE INTERNAL "this is what needs to be included if using iothub_client lib" FORCE)

include_directories(${DEV_AUTH_MODULES_CLIENT_INC_FOLDER})
include_directories(${SHARED_UTIL_INC_FOLDER})
include_directories(${CMAKE_SOURCE_DIR}/azure-iot-sdk-c/deps/parson)
include_directories(${UHTTP_C_INC_FOLDER})
include_directories(${IOTHUB_CLIENT_INC_FOLDER})
include_directories(${CMAKE_SOURCE_DIR}/azure-iot-sdk-c/provisioning_client/adapters)

function(link_security_client whatExeIsBuilding)
    target_link_libraries(${whatExeIsBuilding} prov_auth_client)
    target_link_libraries(${whatExeIsBuilding} hsm_security_client)
endfunction()

function(add_sample_directory whatIsBuilding)
	add_subdirectory(${whatIsBuilding})

	set_target_properties(${whatIsBuilding}
			   PROPERTIES
			   FOLDER "provisioning_client_samples")
endfunction()

add_sample_directory(prov_dev_client_sample)

