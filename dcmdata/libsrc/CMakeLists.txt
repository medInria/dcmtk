# create library from source files
ADD_LIBRARY(dcmdata cmdlnarg dcbytstr dcchrstr dccodec dcdatset dcddirif dcdicdir dcdicent dcdict dcdictzz dcdirrec dcelem dcerror dcfilefo dchashdi dcistrma dcistrmb dcistrmf dcistrmz dcitem dclist dcmetinf dcobject dcostrma dcostrmb dcostrmf dcostrmz dcpcache dcpixel dcpixseq dcpxitem dcrleccd dcrlecce dcrlecp dcrledrg dcrleerg dcrlerp dcsequen dcstack dcswap dctag dctagkey dctypes dcuid dcwcache dcvm dcvr dcvrae dcvras dcvrat dcvrcs dcvrda dcvrds dcvrdt dcvrfd dcvrfl dcvris dcvrlo dcvrlt dcvrobow dcvrof dcvrpn dcvrpobw dcvrsh dcvrsl dcvrss dcvrst dcvrtm dcvrui dcvrul dcvrulup dcvrus dcvrut dcxfer dcpath vrscan vrscanl)

target_link_libraries(dcmdata
oflog
)

if (UNIX OR APPLE)
  target_link_libraries(dcmdata
  z
  )
endif()

# declare installation files
INSTALL_TARGETS(${INSTALL_LIBDIR} dcmdata)
