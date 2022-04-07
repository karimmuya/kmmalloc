# kmalloc

kmalloc is a simple memory allocator.

#### Compile ####
```
gcc -o kmalloc.so -fPIC -shared kmalloc.c
```

#### Usage ####
Using kmalloc is simple, set the enivornment variable ```LD_PRELOAD``` to the path of a shared object compiled so it is loaded before any other library, this trick will load our compiled library (```kmalloc.so```) first so that the later commands run in the shell will use our malloc(), free(), calloc() and realloc().
```
export LD_PRELOAD=$PWD/kmalloc.so
```
Once you're done experimenting, you can do ```unset LD_PRELOAD``` to stop using our allocator.

