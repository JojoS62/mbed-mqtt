add_library(MQTT_packet INTERFACE)

target_include_directories(MQTT_packet INTERFACE ${CMAKE_CURRENT_SOURCE_DIR})

list(APPEND SOURCEFILES 
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


target_sources(MQTT_packet
    INTERFACE
        ${SOURCEFILES}
)

