
## code 

This macro was used to fuse multiple snapshots (without Z or time points) but with the same amount of channels into ONE single multi-point ND file. ^d668ad

```c
// Open the choice menu of documents to merge -> they will be merged as timelapse
MergeOpenedDocuments("");

//Get the size of the timelapse and exchange the dimensions to transform it into multipoint document
ND_ExchangeDimensions(0,ND_GetExperimentLoopSize(1,1),0,0.00000,ACC_ZAbsolute,ACC_ZAbsolute,ACC_ZAbsolute,"",0.00000);
```

^6df04b

