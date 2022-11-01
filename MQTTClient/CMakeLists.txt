add_library(MQTT_client INTERFACE)

target_include_directories(MQTT_client INTERFACE ${CMAKE_CURRENT_SOURCE_DIR})

list(APPEND SOURCEFILES 
    MQTTThreadedClient.cpp
)


target_sources(MQTT_client
    INTERFACE
        ${SOURCEFILES}
)

target_link_libraries(MQTT_client INTERFACE MQTT_packet)