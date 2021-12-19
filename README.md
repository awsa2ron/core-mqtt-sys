export LD_LIBRARY_PATH=/home/ANT.AMAZON.COM/kaixu/repos/rust/core-mqtt-agent/coreMQTT/build/lib
cp ../interface/transport_interface.h ./
cp core_mqtt_config_defaults.h core_mqtt_config.h

sudo cp coreMQTT/build/lib/libcore_mqtt.a /usr/lib/
