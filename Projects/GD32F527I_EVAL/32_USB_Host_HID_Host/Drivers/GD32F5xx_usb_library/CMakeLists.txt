project(GD32F5xx_usb_library LANGUAGES C CXX ASM)

# Comment-out unused source files.
add_library(GD32F5xx_usb_library OBJECT
    # ${DRIVERS_DIR}/GD32F5xx_usb_library/device/class/audio/Source/audio_core.c
    # ${DRIVERS_DIR}/GD32F5xx_usb_library/device/class/audio/Source/audio_out_itf.c
    # ${DRIVERS_DIR}/GD32F5xx_usb_library/device/class/cdc/Source/cdc_acm_core.c
    # ${DRIVERS_DIR}/GD32F5xx_usb_library/device/class/dfu/Source/dfu_core.c
    # ${DRIVERS_DIR}/GD32F5xx_usb_library/device/class/dfu/Source/dfu_mem.c
    # ${DRIVERS_DIR}/GD32F5xx_usb_library/device/class/hid/Source/custom_hid_core.c
    # ${DRIVERS_DIR}/GD32F5xx_usb_library/device/class/hid/Source/standard_hid_core.c
    # ${DRIVERS_DIR}/GD32F5xx_usb_library/device/class/iap/Source/usb_iap_core.c
    # ${DRIVERS_DIR}/GD32F5xx_usb_library/device/class/msc/Source/usbd_msc_bbb.c
    # ${DRIVERS_DIR}/GD32F5xx_usb_library/device/class/msc/Source/usbd_msc_core.c
    # ${DRIVERS_DIR}/GD32F5xx_usb_library/device/class/msc/Source/usbd_msc_scsi.c
    # ${DRIVERS_DIR}/GD32F5xx_usb_library/device/class/printer/Source/printer_core.c
    # ${DRIVERS_DIR}/GD32F5xx_usb_library/device/core/Source/usbd_core.c
    # ${DRIVERS_DIR}/GD32F5xx_usb_library/device/core/Source/usbd_enum.c
    # ${DRIVERS_DIR}/GD32F5xx_usb_library/device/core/Source/usbd_transc.c
    # ${DRIVERS_DIR}/GD32F5xx_usb_library/driver/Source/drv_usbd_int.c
    ${DRIVERS_DIR}/GD32F5xx_usb_library/driver/Source/drv_usbh_int.c
    ${DRIVERS_DIR}/GD32F5xx_usb_library/driver/Source/drv_usb_core.c
    # ${DRIVERS_DIR}/GD32F5xx_usb_library/driver/Source/drv_usb_dev.c
    ${DRIVERS_DIR}/GD32F5xx_usb_library/driver/Source/drv_usb_host.c
    ${DRIVERS_DIR}/GD32F5xx_usb_library/host/class/hid/Source/usbh_hid_core.c
    ${DRIVERS_DIR}/GD32F5xx_usb_library/host/class/hid/Source/usbh_standard_hid.c
    # ${DRIVERS_DIR}/GD32F5xx_usb_library/host/class/msc/Source/usbh_msc_bbb.c
    # ${DRIVERS_DIR}/GD32F5xx_usb_library/host/class/msc/Source/usbh_msc_core.c
    # ${DRIVERS_DIR}/GD32F5xx_usb_library/host/class/msc/Source/usbh_msc_fatfs.c
    # ${DRIVERS_DIR}/GD32F5xx_usb_library/host/class/msc/Source/usbh_msc_scsi.c
    ${DRIVERS_DIR}/GD32F5xx_usb_library/host/core/Source/usbh_core.c
    ${DRIVERS_DIR}/GD32F5xx_usb_library/host/core/Source/usbh_enum.c
    ${DRIVERS_DIR}/GD32F5xx_usb_library/host/core/Source/usbh_pipe.c
    ${DRIVERS_DIR}/GD32F5xx_usb_library/host/core/Source/usbh_transc.c
    )

# Comment-out unused header folders.
target_include_directories(GD32F5xx_usb_library PUBLIC
    # ${DRIVERS_DIR}/GD32F5xx_usb_library/device/class/audio/Include
    # ${DRIVERS_DIR}/GD32F5xx_usb_library/device/class/cdc/Include
    # ${DRIVERS_DIR}/GD32F5xx_usb_library/device/class/dfu/Include
    # ${DRIVERS_DIR}/GD32F5xx_usb_library/device/class/hid/Include
    # ${DRIVERS_DIR}/GD32F5xx_usb_library/device/class/iap/Include
    # ${DRIVERS_DIR}/GD32F5xx_usb_library/device/class/msc/Include
    # ${DRIVERS_DIR}/GD32F5xx_usb_library/device/class/printer/Include
    # ${DRIVERS_DIR}/GD32F5xx_usb_library/device/core/Include
    ${DRIVERS_DIR}/GD32F5xx_usb_library/driver/Include
    ${DRIVERS_DIR}/GD32F5xx_usb_library/host/class/hid/Include
    # ${DRIVERS_DIR}/GD32F5xx_usb_library/host/class/msc/Include
    ${DRIVERS_DIR}/GD32F5xx_usb_library/host/core/Include
    # ${DRIVERS_DIR}/GD32F5xx_usb_library/ustd/class/cdc
    ${DRIVERS_DIR}/GD32F5xx_usb_library/ustd/class/hid
    # ${DRIVERS_DIR}/GD32F5xx_usb_library/ustd/class/msc
    ${DRIVERS_DIR}/GD32F5xx_usb_library/ustd/common
    )

target_link_libraries(GD32F5xx_usb_library PUBLIC GD32F527I_EVAL)
