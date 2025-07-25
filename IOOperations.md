### Why IO operations are slow ?

 - Accessing RAM takes just nano seconds. But when dealing with disk or network operations, it takes milliseconds. So, IO operations are slow compared to CPU operations.

- RAM can transfer data at GB/s, where as disk can transfer data at MB/s.

- IO operations can slow down the performance of the application. So, it is important to optimize IO operations.

- When thread hits the IO operation like an API call, database call or disk write, it gets block.
During IO operation, CPU sits idle.

- Every thread needs memory and CPU resources. And when thread hits the IO operation it just sits there and doing nothing. Zero CPU usage and just waiting.

- So, when multiple threads are created then lot of resources and memory are consumed. It may result in Out of memory, race condition, deadlocks or live locks. Also CPU needs to switch between those threads.

- As a result more threads looks good but actually it slows down the performance more.

- This IO heavy operation can be handled more efficiently via Event Demultiplexer.
