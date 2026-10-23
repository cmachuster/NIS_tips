
## code 

> [!IMPORTANT] To convert multiple single images into a multi-point ND

^065ab3

```c
// Open the choice menu of documents to merge -> they will be merged as timelapse
MergeOpenedDocuments("");

//Get the size of the timelapse and exchange the dimensions to transform it into multipoint document
ND_ExchangeDimensions(0,ND_GetExperimentLoopSize(1,1),0,0.00000,ACC_ZAbsolute,ACC_ZAbsolute,ACC_ZAbsolute,"",0.00000);
```

^6df04b

