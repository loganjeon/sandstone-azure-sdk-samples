# sandstone-azure-sdk-samples
Sample applications using Azure SDK


## Used Azure SDKs

### azure-event-hubs-c
repository : https://github.com/Azure/azure-event-hubs-c.git

version : 0.12.0

### azure-iot-sdk-c
repository : https://github.com/Azure/azure-iot-sdk-c.git

version : LTS_02_2020_Ref01

### azure-storage-cpp
repository : https://github.com/Azure/azure-storage-cpp.git

version : v7.2.0


## Build

### Download sample source and sdk using submodule update
```
git clone [repository url of sandstone-azure-sdk-sample]
cd sandstone-azure-sdk-sample
git submodule update --init --recursive
```

### Run cmake for making build script in each directories
```
cd azure-eventhub
mkdir cmake ; cd cmake ; cmake ..
cd ../..

cd azure-iothub
mkdir cmake ; cd cmake ; cmake -Dhsm_type_symm_key:BOOL=ON -Duse_prov_client:BOOL=ON ..
cd ../..

cd azure-storage
mkdir cmake ; cd cmake ; cmake ..
cd ../..
```

### Build each sample using made build script
