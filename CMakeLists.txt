cmake_minimum_required(VERSION 3.15)
project(MQTTest)

find_package(PahoMqttCpp REQUIRED)
 
add_executable(publisher src/publisher.cpp)
add_executable(consumer src/consumer.cpp)
 
target_link_libraries(publisher paho-mqtt3a paho-mqttpp3)
target_link_libraries(consumer paho-mqtt3a paho-mqttpp3)