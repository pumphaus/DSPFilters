project(DspFilters)

set(DspFilters_SRC
    Bessel.cpp
    Biquad.cpp
    Butterworth.cpp
    Cascade.cpp
    ChebyshevI.cpp
    ChebyshevII.cpp
    Custom.cpp
    Design.cpp
    Documentation.cpp
    Elliptic.cpp
    Filter.cpp
    Legendre.cpp
    Param.cpp
    PoleFilter.cpp
    RASTA.cpp
    RBJ.cpp
    RootFinder.cpp
    State.cpp
)

include_directories(${CMAKE_CURRENT_SOURCE_DIR})
add_library(DSPFilters SHARED ${DspFilters_SRC})
target_link_libraries(DSPFilters)

install(TARGETS DSPFilters
        RUNTIME DESTINATION bin
        LIBRARY DESTINATION lib
        ARCHIVE DESTINATION lib)
install(DIRECTORY DspFilters DESTINATION include)
