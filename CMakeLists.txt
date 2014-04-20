cmake_minimum_required(VERSION 2.7)

include_directories(galib)

add_executable(pngwolf
pngwolf.cxx
galib/ga/GA1DArrayGenome.C
galib/ga/GAAllele.C
galib/ga/GABaseGA.C
galib/ga/gabincvt.C
galib/ga/GAGenome.C
galib/ga/GAIncGA.C
galib/ga/GAParameter.C
galib/ga/GAPopulation.C
galib/ga/garandom.C
galib/ga/gaerror.C
galib/ga/GAScaling.C
galib/ga/GASelector.C
galib/ga/GAStatistics.C
)
find_package( ZLIB REQUIRED )
if ( ZLIB_FOUND )
    include_directories( ${ZLIB_INCLUDE_DIRS} )
    target_link_libraries( pngwolf ${ZLIB_LIBRARIES} )
endif( ZLIB_FOUND )