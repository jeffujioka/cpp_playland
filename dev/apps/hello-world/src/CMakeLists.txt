# TODO add Copyright

file(GLOB_RECURSE SOURCES LIST_DIRECTORIES true *.h *.cpp)

ADD_JMF_EXECUTABLE(
  NAME               ${JMF_MODULE_NAME}
  SRC                ${SOURCES}
  SYS_INCLUDE_DIRS   SYSTEM
  INCLUDE_DIRS       ${CMAKE_CURRENT_SOURCE_DIR}
  LINKER_FLAGS  
  DEPS
  )
  
set(JMF_MODULE_LIB_NAME ${JMF_UNIT_TEST_PREFIX}${JMF_MODULE_NAME})

ADD_JMF_LIB_MODULE(
    NAME               ${JMF_MODULE_LIB_NAME}
    SRC                ${SOURCES}
    SYS_INCLUDE_DIRS   SYSTEM
    INCLUDE_DIRS       ${CMAKE_CURRENT_SOURCE_DIR}
    DEPS
)
