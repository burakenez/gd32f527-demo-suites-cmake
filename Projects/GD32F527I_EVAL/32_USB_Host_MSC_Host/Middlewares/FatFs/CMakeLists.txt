project(FatFs LANGUAGES C CXX ASM)

# Comment-out unused source files.
add_library(FatFs OBJECT
    # ${MIDDLEWARES_DIR}/Third_Party/FatFs/source/diskio.c
    ${MIDDLEWARES_DIR}/Third_Party/FatFs/source/ff.c
    # ${MIDDLEWARES_DIR}/Third_Party/FatFs/source/ffsystem.c
    ${MIDDLEWARES_DIR}/Third_Party/FatFs/source/ffunicode.c
    )

target_include_directories(FatFs PUBLIC
    ${MIDDLEWARES_DIR}/Third_Party/FatFs/source
    
    # Added for "ffconf.h"
    ${CMAKE_SOURCE_DIR}/Application/Core/Inc
    )
