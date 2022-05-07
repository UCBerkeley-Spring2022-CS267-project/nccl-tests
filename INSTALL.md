compile
```
make CUDA_HOME="/usr/local/cuda-11.5" NCCL_HOME=/home/eecs/mengyibai/yefan/nccl-BLINKplus/build
```

run 
```
./build/broadcast_perf --nthreads 1 --ngpus 2 -b 4M -e 128M -f 2
```