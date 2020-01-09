How to copy files from the cluster to cloud without downloading on the terminal. 

We will use rconfig, if not downloaded on the computer, get it. 

First we need to set up the connections to both, cluster and cloud. To do so, we will use 

```{bash}
rclone config
```

We will answer the questions conveniently, depending on the cloud and the cluster (to select the cluster, the type is SSH) that we need to configure.

Then, we are ready to copy.

```{bash}
rclone copy namecluster:foldertocopy namecloud:foldertoputit --progress

rclone copy crg_cluster:332TDP onedrive:Sequencing_data/332TDP --progress
```

--progress is to show us how the copying is going. 

Good things, it will only transfer new/modified files. Files with the same md5 are not recopied. 





