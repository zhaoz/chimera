add_executable(test test.c)
target_link_libraries(test chimera)

add_executable(bighost bighost.c)
target_link_libraries(bighost chimera)

add_executable(bignode bignode.c)
target_link_libraries(bignode chimera)

add_executable(bigtest bigtest.c)
target_link_libraries(bigtest chimera)

#add_executable(bigtest_ssh bigtest_ssh.c)
#target_link_libraries(bigtest_ssh chimera)

#add_executable(chat chat.c)
#target_link_libraries(chat chimera)

add_executable(dht dht.c)
target_link_libraries(dht chimera)

add_executable(dhttest dhttest.c)
target_link_libraries(dhttest chimera)

add_executable(job_test job_test.c)
target_link_libraries(job_test chimera)

add_executable(keygen keygen.c)
target_link_libraries(keygen chimera)

add_executable(monitor monitor.c)
target_link_libraries(monitor chimera)

add_executable(receiver receiver.c)
target_link_libraries(receiver chimera)

#add_executable(routing routing.c)
#target_link_libraries(routing chimera)

add_executable(sender sender.c)
target_link_libraries(sender chimera)

add_executable(sha1_keygen sha1_keygen.c)
target_link_libraries(sha1_keygen chimera)

