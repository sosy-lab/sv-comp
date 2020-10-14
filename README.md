# SV-COMP Replicability
This repository describes the configuration of the competition machines (below)
and the benchmark definition for each verifier (folder benchmark-defs),
in order to make results of the competition more replicable.


## Ubuntu Packages on Apollon Machines

### Docker Image
SV-COMP provides a Docker image that tries to provide an environment
that has mostly the same packages installed as the competition machines:
- Docker definition: https://gitlab.com/sosy-lab/sv-comp/archives-2021/blob/master/Dockerfile.user
- Docker image: `registry.gitlab.com/sosy-lab/sv-comp/archives-2021/user:latest`
- Test if the tool works with the installation:
  - Unzip tool archive to temporary directory `<TOOL>` (`<TOOL>` must be an absolute path)
  - `docker pull registry.gitlab.com/sosy-lab/sv-comp/archives-2021/user:latest`
  - `docker run --rm -i -t --volume=<TOOL>:/tool --workdir=/tool registry.gitlab.com/sosy-lab/sv-comp/archives-2021/user:latest bash`
  - Start tool


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


