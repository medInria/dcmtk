# declare project
PROJECT(dcmimage)

# declare include directories which hold for all subdirectories
INCLUDE_DIRECTORIES(${dcmimage_SOURCE_DIR}/include ${ofstd_SOURCE_DIR}/include ${oflog_SOURCE_DIR}/include ${dcmdata_SOURCE_DIR}/include ${dcmimgle_SOURCE_DIR}/include ${ZLIB_INCDIR} ${LIBTIFF_INCDIR} ${LIBPNG_INCDIR})

# recurse into subdirectories
SUBDIRS(libsrc include/dcmtk/dcmimage)

IF(${DCMTK_BUILD_TOOLS})
    SUBDIRS (apps)
ENDIF()
