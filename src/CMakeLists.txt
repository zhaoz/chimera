SET(LIBCHIMERA 
	chimera.c
	dllist.c
	dtime.c
	host.c
	job_queue.c
	jrb.c
	jval.c
	key.c
	log.c
	message.c
	network.c
	route.c
	semaphore.c)

add_library(chimera ${LIBCHIMERA})
