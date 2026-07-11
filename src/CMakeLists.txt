add_library(
	asteroid-health
	main.cpp
	cpp/lineGraph_p.cpp
	cpp/lineGraph_p.h
	resources.qrc
)
set_target_properties(asteroid-health PROPERTIES PREFIX "")

target_link_libraries(
	asteroid-health
	PUBLIC
		Asteroid::AsteroidApp6
)

install(
	TARGETS asteroid-health
	DESTINATION ${CMAKE_INSTALL_LIBDIR}
)
