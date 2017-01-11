# CacheQueue
This is a simple cache simulator, written in C, which implements a Hash of Queue's.
Below are the instructions given to us, in class, to build this Cache simulator:

In this lab, will you will write a small cache simulator that simulates the behavior of a cache
memory. The input to that cache simulator is a cache configuration and a trace file; and the
output is a set of statistics:
hits: how many cache hits
misses: how many cache misses
evictions: how many blocks have been kicked out of the cache. You need to implement Least
Recently Used (LRU) replacement policy. (Hint: Do not forget the valid bit!)

(to run the code) The command line looks like this:
./cachesim -s <num> -E <num> -b <num> -t <file>
Options:
 -s <num> Number of set index bits
 -E <num> Number of blocks per set (i.e. associativity).
 -b <num> Number of block offset bits.
 -t <file> Trace file.
So
./cachesim -s 10 -E 8 -b 6 -t ls.trace
means this cache has 210 = 1024 sets and each set has 8 blocks (i.e. 8-way set associative) and the
block size is 26 = 64 bytes. The simulator will produce hits, misses, and evictions for the trace
file ls.trace.
