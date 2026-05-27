
# **File structure of QM2 Beamline data**


The output file structure from nxrefine should look something like the following:
Datafile: /nfs/chess/id4baux/2025-2/sarker-0000-a/nxrefine/sample_name/sample_id/RbV3Sb5_14.nxs
```
nfs
└── chess
    └── id4b
        └── 2025-2
            └── chess
                └── sarker-0000-a
                        └── raw6m
                            └── sample_name
                                └── sample_id
                                  └── 14
                                      └── filename_14
                                            └── sample_name_PIL10_009_00001.cbf
                                            └── sample_name_PIL10_009_00002.cbf
                                            └── sample_name_PIL10_009_00001.cbf
                                            └── ...
          
                                  ├── 300
                                      └── filename_300
                                            └── sample_name_PIL10_009_00001.cbf
                                            └── sample_name_PIL10_009_00002.cbf
                                            └── sample_name_PIL10_009_00001.cbf
                                            └── ...
```

The file that we are interested in loading is the .cbf file with the form `sample_name_PIL10_009_00001.cbf`, which holds information
