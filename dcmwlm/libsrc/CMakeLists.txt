# create library from source files
ADD_LIBRARY(dcmwlm wlds wldsfs wlfsim wlmactmg)

target_link_libraries(dcmwlm
dcmnet
)

# declare installation files
INSTALL_TARGETS(${INSTALL_LIBDIR} dcmwlm)
