# Memory Allocator

This project is an implementation of a dynamic storage allocator for C programs, including custom versions of the `malloc` and `free` functions. The allocator is designed to examine the tradeoffs between utilization and throughput, and to improve C programming skills through the use of structs, pointers, macros, and debugging techniques.

The allocator consists of three primary functions, declared in `mm.h` and defined in `mm.c`:

```c
int mm_init(void);
void* mm_malloc(size_t size);
void mm_free(void* ptr);
```

Additionally, the memlib.c package simulates the memory system for the allocator, providing the following functions:

```
void* mem_sbrk(int incr);
void* mem_heap_lo(void);
void* mem_heap_hi(void);
size_t mem_heapsize(void);
size_t mem_pagesize(void);
```

*t <tracedir>: Look for trace files in the specified directory instead of the default directory defined in config.h.
*f <tracefile>: Use a specific trace file for testing instead of the default set of trace files.
*h: Print a summary of the command line arguments.
*l: Run and measure the standard malloc function in addition to the custom allocator.
*v: Verbose output. Print a performance breakdown for each trace file in a compact table.
*V: More verbose output. Print additional diagnostic information as each trace file is processed. This is useful for debugging and determining which trace file is causing issues with the allocator.
