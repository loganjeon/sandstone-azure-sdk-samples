# Written by Yeonggyoo Jeon

include_directories(${MACRO_UTILS_INC_FOLDER})
include_directories(${UAMQP_INC_FOLDER})
include_directories(${UMOCK_C_INC_FOLDER})
include_directories(${SHARED_UTIL_INC_FOLDER})

set(EVENTHUB_CLIENT_INC_FOLDER ${CMAKE_SOURCE_DIR}/azure-event-hubs-c/eventhub_client/inc CACHE INTERNAL "this is what needs to be included if using eventhub_client lib" FORCE)
include_directories(${EVENTHUB_CLIENT_INC_FOLDER})


function(add_sample_directory whatIsBuilding)
	add_subdirectory(${whatIsBuilding})

	set_target_properties(${whatIsBuilding}
			   PROPERTIES
			   FOLDER "eventhub_client_samples")
endfunction()

add_sample_directory(send)

