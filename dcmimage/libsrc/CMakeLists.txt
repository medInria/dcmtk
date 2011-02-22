# create library from source files
ADD_LIBRARY(dcmimage diargimg dicmyimg dicoimg dicoopx dicopx dihsvimg dilogger dipalimg dipipng dipitiff diqtctab diqtfs diqthash diqthitl diqtpbox diquant diregist dirgbimg diybrimg diyf2img diyp2img)

target_link_libraries(dcmimage
${LIBPNG_LIBS}
${LIBTIFF_LIBS}
dcmimgle
)

# declare installation files
INSTALL_TARGETS(${INSTALL_LIBDIR} dcmimage)
