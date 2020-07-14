# Dataset 
There are two ways to get the dataset. 

## Option 1
We provide converted files that are dervied from the Graph Challenge website over a Box. This can be downloaded from (Total of ~90GB): 
[BoxFolder](https://uofi.box.com/s/gseet60dz0f939r6n69veggn80i9twwh)

After download is complete, untar all the files present inside the dataset. 

## Option 2
Automatic download and compilation (requires gzip and tar support).
Space Required: ~300GB. Post processing ~90GB. 

```
mkdir dataset
cd dataset
bash ../download.sh
```

# Dependencies

1. Latest version of CUDA. 
2. mpicxx compiler 

## Installing mpicxx compiler
```
# For CentOS/RedHat system
sudo dnf install mpich mpich-devel

# For Ubuntu system
sudo apt-get install -y mpich
```

`export` the installed mpich binary path and lib paths to `$PATH` and `$LD_LIBRARY_PATH` variables. 

# Run 
After clearing dependencies, run the following. 

```
cd iostream
make -j 
```

Change DATASET environment variable to reflect your downloaded path in `run_local.sh`

```
bash run_local.sh > output.log 
```

Do let us know if you get any errors in output.log. Ideally it should work without any issues. 