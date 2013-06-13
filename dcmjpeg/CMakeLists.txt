# declare project
PROJECT(dcmjpeg)

# recurse into subdirectories
SUBDIRS(libsrc libijg8 libijg12 libijg16 include/dcmtk/dcmjpeg)

IF(${DCMTK_BUILD_TOOLS})
    SUBDIRS (apps)
ENDIF()
