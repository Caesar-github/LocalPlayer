add_definitions("-DACSDK_LOG_MODULE=PlaylistParser")

add_library(PlaylistParser SHARED PlaylistParser.cpp UrlToAttachmentConverter.cpp)

target_include_directories(PlaylistParser PUBLIC
    "${PlaylistParser_SOURCE_DIR}/include" 
    "${ACL_SOURCE_DIR}/include")

target_link_libraries(PlaylistParser LPCommon)

# install target
#asdk_install()
