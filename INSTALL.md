```
make CUDA_HOME="/usr/local/cuda-11.5" NCCL_HOME=/home/eecs/mengyibai/yefan/nccl-BLINKplus/build
./build/broadcast_perf --nthreads 1 --ngpus 4 -b 8 -e 128 -f 2
```