# SV-COMP Replicability
This repository describes the configuration of the competition machines (below)
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

## Ubuntu Packages on Apollon Machines for SV-COMP

### Added Packages
- linux-image-generic
- ubuntu-minimal
- openjdk-8-jre-headless
- gcc-multilib # cpp, development headers
- libgomp1 # for Z3
- make # for fshellw2t
- clang # SV-COMP'19 AProVE
- mono-apache-server # to avoid the mono-xsp dependency of mono-xsp
- mono-complete # SV-COMP'19 AProVE, SMACK
- gcc-5-multilib # SV-COMP'19 PredatorHP
- python # SV-COMP'19 PredatorHP, Symbiotic
- python-lxml # SV-COMP'19 Symbiotic
- linux-libc-dev:i386 # SV-COMP'19 CBMC
- python-sklearn # SV-COMP'19 VeriFuzz
- python-pandas # SV-COMP'19 VeriFuzz
- python-pycparser # SV-COMP'19 CSeq
- unzip # SV-COMP'19 JBMC

