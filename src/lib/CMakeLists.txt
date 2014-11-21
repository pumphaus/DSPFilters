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
    RBJ.cpp
    RootFinder.cpp
    State.cpp
)

set(DspFilters_HEADERS
    DspFilters/Bessel.h
    DspFilters/Biquad.h
    DspFilters/Butterworth.h
    DspFilters/Cascade.h
    DspFilters/ChebyshevI.h
    DspFilters/ChebyshevII.h
    DspFilters/Common.h
    DspFilters/Custom.h
    DspFilters/Design.h
    DspFilters/Dsp.h
    DspFilters/Elliptic.h
    DspFilters/Filter.h
    DspFilters/Layout.h
    DspFilters/Legendre.h
    DspFilters/MathSupplement.h
    DspFilters/Params.h
    DspFilters/PoleFilter.h
    DspFilters/RBJ.h
    DspFilters/RootFinder.h
    DspFilters/SmoothedFilter.h
    DspFilters/State.h
    DspFilters/Types.h
    DspFilters/Utilities.h
)

add_library(DSPFilters SHARED ${DspFilters_SRC})
target_link_libraries(DSPFilters)

install(TARGETS DSPFilters DESTINATION lib)
install(FILES ${DspFilters_HEADERS} DESTINATION include/DspFilters)
