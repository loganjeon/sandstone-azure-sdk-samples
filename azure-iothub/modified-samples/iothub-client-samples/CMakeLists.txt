# Written by Yeonggyoo Jeon

include_directories(${DEV_AUTH_MODULES_CLIENT_INC_FOLDER})
include_directories(${AZURE_C_SHARED_UTILITY_INCLUDES})
include_directories(${SHARED_UTIL_INC_FOLDER})

set(IOTHUB_CLIENT_INC_FOLDER ${CMAKE_SOURCE_DIR}/azure-iot-sdk-c/iothub_client/inc CACHE INTERNAL "this is what needs to be included if using iothub_client lib" FORCE)
include_directories(${IOTHUB_CLIENT_INC_FOLDER})

function(add_sample_directory whatIsBuilding)
	add_subdirectory(${whatIsBuilding})

	set_target_properties(${whatIsBuilding}
			   PROPERTIES
			   FOLDER "iothub_client_samples")
endfunction()

add_sample_directory(iothub_ll_c2d_sample)
