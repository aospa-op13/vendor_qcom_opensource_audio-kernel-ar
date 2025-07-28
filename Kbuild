ifeq ($(CONFIG_ARCH_SUN), y)
	include $(AUDIO_ROOT)/config/sunauto.conf
	export INCS += -include $(AUDIO_ROOT)/config/sunautoconf.h
endif

obj-y := dsp/ ipc/ soc/ asoc/ asoc/codecs/ asoc/codecs/lpass-cdc/ asoc/codecs/bolero/ asoc/codecs/wcd939x/ asoc/codecs/wsa884x/ asoc/codecs/wcd938x/ asoc/codecs/wsa883x/ asoc/codecs/wcd937x/ asoc/codecs/wcd9378/ asoc/codecs/qmp1000/ asoc/codecs/aw87xxx/ asoc/codecs/aw882xx/ asoc/codecs/tfa98xx-v6/ asoc/codecs/sipa/ oplus_speaker_manager/ oplus_audio_daemon/ oplus_audio_netlink/ oplus_typec_switch_i2c/

############ audio extend driver ############

ifdef CONFIG_AUDIO_EXTEND_DRV
AUDIO_EXTEND_OBJS += audio_extend_drv.o
endif

# Module information used by KBuild framework
obj-$(CONFIG_AUDIO_EXTEND_DRV) += oplus_audio_extend.o
oplus_audio_extend-y := $(AUDIO_EXTEND_OBJS)