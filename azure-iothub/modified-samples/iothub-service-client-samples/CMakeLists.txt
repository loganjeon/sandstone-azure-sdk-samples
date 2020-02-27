# Written by Yeonggyoo Jeon

include_directories(${SHARED_UTIL_INC_FOLDER})
include_directories(${UAMQP_INC_FOLDER})
include_directories(${UAMQP_INCLUDES})

set(IOTHUB_SERVICE_CLIENT_INC_FOLDER ${CMAKE_SOURCE_DIR}/azure-iot-sdk-c/iothub_service_client/inc CACHE INTERNAL "This is the include folder for iothub_service_client" FORCE)
include_directories(${CMAKE_SOURCE_DIR}/azure-iot-sdk-c/deps/parson ${IOTHUB_SERVICE_CLIENT_INC_FOLDER} ${CMAKE_SOURCE_DIR}/azure-iot-sdk-c/iothub_client/inc)

function(add_sample_directory whatIsBuilding)
	add_subdirectory(${whatIsBuilding})

	set_target_properties(${whatIsBuilding}
			   PROPERTIES
			   FOLDER "iothub_service_client_samples")
endfunction()

add_sample_directory(iothub_registrymanager_sample)

