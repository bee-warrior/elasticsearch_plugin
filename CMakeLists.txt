file(GLOB HEADERS "include/snax/elasticsearch_plugin/*.hpp")
add_library( elasticsearch_plugin
             elasticsearch_plugin.cpp
             elastic_client.cpp
             bulker.cpp
             ${HEADERS} )

target_link_libraries( elasticsearch_plugin appbase chain_plugin snax_chain fc elasticlient)
target_include_directories( elasticsearch_plugin PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/include" )
