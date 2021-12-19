# core-mqtt-sys

## coreMQTT update
Instructions for updating to new coreMQTT source code releases in `core-mqtt-sys/`:

1. Wipe out `coreMQTT/` and replace it with the contents of the distribution tarball.
2. Cherry-pick any local changes from the previous version.
3. Build coreMQTT to generate libcore_mqtt.a,
   and update libcore_mqtt.a on your system.

```
cd coreMQTT/
rm -rf build && mkdir build
cd build/
cp ../../CMakeLists.txt ../
cmake ..
make
sudo cp lib/libcore_mqtt.a /usr/lib/
```

4. copy `core_mqtt_config_defaults.h` as `core_mqtt_config_defaults.h`.
```
cd ../source/include/
cp core_mqtt_config_defaults.h core_mqtt_config.h
cp ../interface/transport_interface.h ./

```
5. build & test
```
cargo build
cargo test
```
6. Update `Cargo.toml` version number.
