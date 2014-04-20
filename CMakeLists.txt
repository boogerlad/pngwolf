cmake_minimum_required(VERSION 2.7)

include_directories(galib)

add_executable(pngwolf
pngwolf.cxx
galib/GA1DArrayGenome.C
galib/GAAllele.C
galib/GABaseGA.C
galib/gabincvt.C
galib/GAGenome.C
galib/GAIncGA.C
galib/GAParameter.C
galib/GAPopulation.C
galib/garandom.C
galib/gaerror.C
galib/GAScaling.C
galib/GASelector.C
galib/GAStatistics.C
)
find_package( ZLIB REQUIRED )
if ( ZLIB_FOUND )
    include_directories( ${ZLIB_INCLUDE_DIRS} )
    target_link_libraries( pngwolf ${ZLIB_LIBRARIES} )
endif( ZLIB_FOUND )