set(LIBFASTCOMMON_SRC
hash.c
chain.c
shared_func.c
ini_file_reader.c
logger.c
sockopt.c
base64.c
sched_thread.c
http_func.c
md5.c
pthread_func.c
local_ip_func.c
avl_tree.c
ioevent.c
ioevent_loop.c
fast_task_queue.c
fast_timer.c
process_ctrl.c
fast_mblock.c
connection_pool.c
fast_mpool.c
fast_allocator.c
fast_buffer.c
multi_skiplist.c
flat_skiplist.c
system_info.c
fast_blocked_queue.c
id_generator.c
char_converter.c
char_convert_loader.c
)

SET(HEADER_FILE
common_define.h 
hash.h 
chain.h 
logger.h base64.h 
shared_func.h pthread_func.h ini_file_reader.h _os_define.h 
sockopt.h sched_thread.h http_func.h md5.h local_ip_func.h 
avl_tree.h ioevent.h ioevent_loop.h fast_task_queue.h 
fast_timer.h process_ctrl.h fast_mblock.h 
connection_pool.h fast_mpool.h fast_allocator.h 
fast_buffer.h skiplist.h multi_skiplist.h flat_skiplist.h 
skiplist_common.h system_info.h fast_blocked_queue.h 
php7_ext_wrapper.h id_generator.h char_converter.h 
char_convert_loader.h
)


add_library(fastcommon  STATIC ${LIBFASTCOMMON_SRC} )
add_library(fastcommon_static  SHARED ${LIBFASTCOMMON_SRC} )
SET_TARGET_PROPERTIES(fastcommon_static PROPERTIES OUTPUT_NAME fastcommon  DESTINATION  lib)



INSTALL(TARGETS   fastcommon fastcommon_static  DESTINATION lib)
INSTALL(FILES     fastcommon fastcommon_static  DESTINATION lib)
