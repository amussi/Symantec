## Volume replicator - Command reference


### Replication status 

``` 
# vradmin -g apache -l repstatus apache_rvg 
Replicated Data Set: apache_rvg
Primary:
  Host name:                  node05-rep
  RVG name:                   apache_rvg
  DG name:                    apache
  RVG state:                  enabled for I/O
  Data volumes:               9
  VSets:                      0
  SRL name:                   srl
  SRL size:                   278.38 G
  Total secondaries:          1
Secondary:
  Host name:                  node06-rep
  RVG name:                   apache_rvg
  DG name:                    apache
  Rlink from Primary:         to_node06
  Rlink to Primary:           to_node05
  Configured mode:            asynchronous
  Latency protection:         override
  SRL protection:             autodcm
  Data status:                consistent, up-to-date
  Replication status:         replicating (connected)
  Current mode:               asynchronous
  Logging to:                 SRL
  Timestamp Information:      behind by  0h 0m 0s
  Bandwidth Limit:            N/A
  Compression Mode:           Off
```


### Checking configuration 

```
# vradmin -g apache printrvg apache_rvg
Replicated Data Set: apache_rvg
Primary:
        HostName: node05-rep    <localhost>
        RvgName: apache_rvg
        DgName: apache
Secondary:
        HostName: node06-rep
        RvgName: apache_rvg
        DgName: apache
```

### Checking object in vvr

```
# vradmin -g apache printvol apache_rvg 
Replicated Data Set: apache_rvg
TY  PRIMARY                               SECONDARY
h   node05-rep                         node06-rep
dg  apache                                apache
rv  apache_rvg                            apache_rvg
v   root                                  root
sz  1024000                               1024000
pn  1                                     1
fl  DCM                                   DCM
v   apache-bin                            apache-bin
sz  204800                                204800
pn  1                                     1
fl  DCM                                   DCM
v   apache-etc                            apache-etc
sz  2097152                               2097152
pn  1                                     1
fl  DCM                                   DCM
v   apache-include                        apache-include
sz  204800                                204800
pn  1                                     1
fl  DCM                                   DCM
v   apache-lib                            apache-lib
sz  204800                                204800
pn  1                                     1
fl  DCM                                   DCM
v   apache-openssl                        apache-openssl
sz  204800                                204800
pn  1                                     1
fl  DCM                                   DCM
v   apache-share                          apache-share
sz  204800                                204800
pn  1                                     1
fl  DCM                                   DCM
v   apache-apache                         apache-apache
sz  1024000                               1024000
pn  1                                     1
fl  DCM                                   DCM
v   apache-var                            apache-var
sz  8773220352                            8773220352
pn  1                                     1
fl  DCM                                   DCM
``` 
