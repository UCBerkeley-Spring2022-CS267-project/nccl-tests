

## Compile on RISE
```
make -j 60 CUDA_HOME="/usr/local/cuda-11.5" NCCL_HOME=/home/eecs/mengyibai/xiaosx/blinkplus-nccl-base/build NVCC_GENCODE="-gencode=arch=compute_70,code=sm_70"
```

note: we're using single processor single thread, and thus do not need MPI support.


## On Experiment
```
./build/broadcast_perf --nthreads 1 --ngpus 2 -b 4M -e 128M -f 2

./build/broadcast_perf --nthreads 1 --ngpus 2 -b 4M -e 128M -f 2 -d int8 -c 0 -n 30

./build/all_reduce_perf --nthreads 1 --ngpus 2 -b 4M -e 1024M -f 2 -d int8 -c 0 -n 30
```