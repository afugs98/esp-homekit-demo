PROGRAM = wifi_config

EXTRA_COMPONENTS = \
	extras/http-parser \
	extras/dhcpserver \
	extras/i2s_dma \
	extras/ws2812_i2s \
	$(abspath ../../components/wifi_config) \
	$(abspath ../../components/wolfssl) \
	$(abspath ../../components/cJSON) \
	$(abspath ../../components/homekit)

FLASH_SIZE ?= 32

EXTRA_CFLAGS += -I../.. -DHOMEKIT_SHORT_APPLE_UUIDS

include $(SDK_PATH)/common.mk

LIBS += m

monitor:
	$(FILTEROUTPUT) --port $(ESPPORT) --baud 115200 --elf $(PROGRAM_OUT)
