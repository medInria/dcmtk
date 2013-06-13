# declare project
PROJECT(dcmjpls)

# recurse into subdirectories
SUBDIRS(libsrc libcharls include/dcmtk/dcmjpls)

IF(${DCMTK_BUILD_TOOLS})
    SUBDIRS (apps)
ENDIF()
