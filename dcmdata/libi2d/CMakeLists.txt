# create library from source files
ADD_LIBRARY(i2d i2d i2dplvlp i2djpgs i2dbmps i2dplsc i2dplnsc)

target_link_libraries(i2d
dcmdata
)

# declare installation files
INSTALL_TARGETS(${INSTALL_LIBDIR} i2d)
