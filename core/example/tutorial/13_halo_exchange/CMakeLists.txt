  add_executable(HaloExchange halo_exchange_example.cpp)
  target_link_libraries(HaloExchange cabanacore)
  add_test(NAME Core_tutorial_13 COMMAND ${MPIEXEC} ${MPIEXEC_NUMPROC_FLAG}
    ${MPIEXEC_MAX_NUMPROCS} ${MPIEXEC_PREFLAGS} ${CMAKE_CURRENT_BINARY_DIR}/HaloExchange ${MPIEXEC_POSTFLAGS})
  set_tests_properties(Core_tutorial_13 PROPERTIES PROCESSORS ${MPIEXEC_MAX_NUMPROCS})
