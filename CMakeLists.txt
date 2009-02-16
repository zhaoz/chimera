cmake_minimum_required(VERSION 2.6)

project(CHIMERA)

LINK_LIBRARIES(pthread ssl)

include_directories(${CHIMERA_SOURCE_DIR}/include)
add_subdirectory(src)
add_subdirectory(test)

SET(EXECUTABLE_OUTPUT_PATH ${PROJECT_BINARY_DIR}/out/bin)
SET(LIBRARY_OUTPUT_PATH ${PROJECT_BINARY_DIR}/out/lib)

SET(LIBCHIMERA 
	src/chimera.c
	src/dllist.c
	src/dtime.c
	src/host.c
	src/job_queue.c
	src/jrb.c
	src/jval.c
	src/key.c
	src/log.c
	src/message.c
	src/network.c
	src/route.c
	src/semaphore.c)

ADD_DEFINITIONS(-fPIC)


add_library(chimera ${LIBCHIMERA})

add_executable(test test/test.c)
target_link_libraries(test chimera)

add_executable(bighost test/bighost.c)
target_link_libraries(bighost chimera)

add_executable(bignode test/bignode.c)
target_link_libraries(bignode chimera)

add_executable(bigtest test/bigtest.c)
target_link_libraries(bigtest chimera)

#add_executable(bigtest_ssh test/bigtest_ssh.c)
#target_link_libraries(bigtest_ssh chimera)

#add_executable(chat test/chat.c)
#target_link_libraries(chat chimera)

add_executable(dht test/dht.c)
target_link_libraries(dht chimera)

add_executable(dhttest test/dhttest.c)
target_link_libraries(dhttest chimera)

add_executable(job_test test/job_test.c)
target_link_libraries(job_test chimera)

add_executable(keygen test/keygen.c)
target_link_libraries(keygen chimera)

add_executable(monitor test/monitor.c)
target_link_libraries(monitor chimera)

add_executable(receiver test/receiver.c)
target_link_libraries(receiver chimera)

#add_executable(routing test/routing.c)
#target_link_libraries(routing chimera)

add_executable(sender test/sender.c)
target_link_libraries(sender chimera)

add_executable(sha1_keygen test/sha1_keygen.c)
target_link_libraries(sha1_keygen chimera)

