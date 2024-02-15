add_library(MQTT_client STATIC
    MQTTThreadedClient.cpp
)

target_include_directories(MQTT_client INTERFACE .)


target_link_libraries(MQTT_client PUBLIC 
    mbed-rtos-flags
    MQTT_packet
)