# declare project
PROJECT(dcmsign)

# declare include directories which hold for all subdirectories
INCLUDE_DIRECTORIES(${dcmsign_SOURCE_DIR}/include ${ofstd_SOURCE_DIR}/include ${oflog_SOURCE_DIR}/include ${dcmdata_SOURCE_DIR}/include ${ZLIB_INCDIR} ${OPENSSL_INCDIR})

# recurse into subdirectories
SUBDIRS(libsrc include/dcmtk/dcmsign)

IF(${DCMTK_BUILD_TOOLS})
    SUBDIRS (apps)
ENDIF()
