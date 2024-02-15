add_library(mbed-mqtt INTERFACE)

add_subdirectory(MQTTClient)
add_subdirectory(MQTTPacket)

target_link_libraries(mbed-mqtt INTERFACE
    MQTT_client
)

