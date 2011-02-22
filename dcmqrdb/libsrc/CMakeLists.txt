# create library from source files
ADD_LIBRARY(dcmqrdb dcmqrcbf dcmqrcbg dcmqrcbm dcmqrcbs dcmqrcnf dcmqrdbi dcmqrdbs dcmqropt dcmqrptb dcmqrsrv dcmqrtis)

target_link_libraries(dcmqrdb
dcmnet
dcmdata
)

# declare installation files
INSTALL_TARGETS(${INSTALL_LIBDIR} dcmqrdb)
