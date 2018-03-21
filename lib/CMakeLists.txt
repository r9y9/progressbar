configure_file(../progressbar.pc.in "${PROJECT_BINARY_DIR}/progressbar.pc" @ONLY)

add_library(progressbar progressbar.c)
add_library(statusbar statusbar.c)

install(FILES "${PROJECT_BINARY_DIR}/progressbar.pc" DESTINATION lib/pkgconfig/)
install(TARGETS progressbar DESTINATION lib RUNTIME DESTINATION bin)
install(TARGETS statusbar DESTINATION lib RUNTIME DESTINATION bin)
install(DIRECTORY ../include/progressbar DESTINATION include PATTERN "*.in" EXCLUDE)
