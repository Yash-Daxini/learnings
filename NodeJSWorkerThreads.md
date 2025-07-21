### Node JS Worker Threads

- By default node js works on single thread, it means it executes one task at a time. But it handles IO heavy tasks efficiently using event loop and libuv.

- All the tasks are start execution with call stack where execution takes place by one task at a time.

- Libuv handles all async tasks in the background. Libuv places the IO task into task queue and then one of the threads in libuv's thread pull, usually 4 threads by default, will pick up task and process the threads in background. This threads don't run javascript logic, they are purely for handling system level operations like file system, network, etc. Once the task is completed, libuv uses event demultiplexer to notify the system or main thread that the IO task is done. Event loop picks up the task from event queue and callback associated with the IO operation is sent back to call stack.

- Libuv threads don't run javascript code, they are just for handling system level operations like file system, network, etc.

- Worker threads: It allows to run javascript code in parallel on separate threads without blocking the main event loop.
