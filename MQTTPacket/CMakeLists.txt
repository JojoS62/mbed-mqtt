add_library(MQTT_packet STATIC
    MQTTConnectClient.c
    MQTTConnectServer.c
    MQTTDeserializePublish.c
    MQTTFormat.c
    MQTTPacket.c
    MQTTSerializePublish.c
    MQTTSubscribeClient.c
    MQTTSubscribeServer.c
    MQTTUnsubscribeClient.c
    MQTTUnsubscribeServer.c
)

target_link_libraries(MQTT_packet PUBLIC
    mbed-core-flags
    mbed-netsocket
)

target_include_directories(MQTT_packet INTERFACE ${CMAKE_CURRENT_SOURCE_DIR})


