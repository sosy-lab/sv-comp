# SV-COMP Replicability
This repository describes the configuration of the competition machines (below)
and the benchmark definition for each verifier (folder benchmark-defs),
in order to make results from SV-COMP more replicable.


## Ubuntu Packages on Apollon Machines for Test-Comp

### Docker Image
SV-COMP provides a Docker image that tries to provide an environment
that has mostly the same packages installed as the competition machines:
- Docker image: registry.gitlab.com/sosy-lab/sv-comp/archives-2020/user:latest
- Docker definition: https://gitlab.com/sosy-lab/sv-comp/archives-2020/blob/master/Dockerfile.user

### Additional Packages on Apollon Machines
The following packages are not installed in the Docker image, but on the competition machines:
- linux-image-generic
- ubuntu-minimal


## Parameters of RunExec for SV-COMP
```
--container
--read-only-dir /
--hidden-dir /home
--overlay-dir /etc
--hidden-dir /var/lib/cloudy # environment-specific
--set-cgroup-value pids.max=5000
--output-directory <work-dir>
--overlay-dir <run-dir>
--debug
--maxOutputSize 2MB
--dir <work-dir>
--output <logfile>
--timelimit <depends on benchmark XML>
--softtimelimit 900s # only if specified in benchmark XML
--memlimit 15GB
--memoryNodes 0 # hardware-specific
--cores 0-7 # hardware-specific
```


