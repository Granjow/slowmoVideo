
set(SRCS
    testFlowRW_sV.cpp
    testFlowField_sV.cpp
    testVector_sV.cpp
    testIntMatrix_sV.cpp
    testXmlProjectRW_sV.cpp
    testDefs_sV.cpp
    testShutterFunction_sV.cpp
    testProject_sV.cpp
    testNodeList_sV.cpp
    testAll.cpp
)
set(SRCS_MOC
    testFlowRW_sV.h
    testFlowField_sV.h
    testVector_sV.h
    testIntMatrix_sV.h
    testDefs_sV.h
    testShutterFunction_sV.h
    testXmlProjectRW_sV.h
    testNodeList_sV.h
    testProject_sV.h
)

qt4_wrap_cpp(MOC_OUT ${SRCS_MOC})

add_executable(UnitTests ${SRCS} ${MOC_OUT})
target_link_libraries(UnitTests sVproj ${EXTERNAL_LIBS})
