# SV-COMP Replicability
This repository describes the configuration of the competition (below)
and the benchmark definition for each verifier (folder benchmark-defs),
in order to make results from SV-COMP more replicability.

## Parameters of RunExec for SV-COMP
```
--container
--read-only-dir /
--hidden-dir /home
--overlay-dir /etc
--hidden-dir /sys/kernel/debug
--hidden-dir /var/lib/cloudy
--read-only-dir /run/systemd/resolve
--set-cgroup-value pids.max=5000
--filesSizeLimit 15GB
--filesCountLimit 10000
```

## Ubuntu Package on Apollon Machines for SV-COMP

### Added Packages
- linux-image-generic
- ubuntu-minimal
- openjdk-8-jre-headless
- gcc-multilib
- libgomp1
- make
- clang
- mono-apache-server
- mono-complete
- gcc-5-multilib
- python
- python-lxml
- linux-libc-dev:i386
- python-sklearn
- python-pandas
- python-pycparser
- unzip


