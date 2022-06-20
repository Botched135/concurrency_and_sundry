set(lock_lib cas_locks)
add_library(${lock_lib} INTERFACE)
add_library(botched135::locks ALIAS ${lock_lib} )


target_compile_features(${lock_lib} INTERFACE cxx_std_20)
target_include_directories(${lock_lib} INTERFACE
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}>
    $<INSTALL_INTERFACE:include/)