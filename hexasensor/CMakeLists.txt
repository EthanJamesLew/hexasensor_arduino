set(ARDUINO_DEFAULT_BOARD diecimila) # Default Board ID, when not specified
set(ARDUINO_DEFAULT_PORT /dev/ttyACM0) # Default Port, when not specified

include_directories(${Hexasensor_SOURCE_DIR}/adafruit)
LINK_DIRECTORIES(${Hexasensor_SOURCE_DIR}/adafruit)
link_libraries(adafruit)

generate_arduino_firmware(hexasensor
    SRCS main.cpp
    LIBS adafruit
    BOARD uno)

