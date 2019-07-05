# SV-COMP Replicability
This repository describes the configuration of the competition machines (below)
and the benchmark definition for each verifier (folder benchmark-defs),
in order to make results from SV-COMP more replicable.

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

## Ubuntu Packages on Apollon Machines for SV-COMP

### Added Packages
- linux-image-generic
- ubuntu-minimal
- openjdk-11-jdk-headless
- gcc-multilib *// cpp, development headers*
- libgomp1 *// for Z3*
- make *// for fshellw2t*
- clang *// SV-COMP'19 AProVE*
- mono-devel *// SV-COMP'19 AProVE, SMACK*
- gcc-5-multilib *// SV-COMP'19 PredatorHP*
- python *// SV-COMP'19 PredatorHP, Symbiotic*
- python-lxml *// SV-COMP'19 Symbiotic*
- linux-libc-dev:i386 *// SV-COMP'19 CBMC*
- python-sklearn *// SV-COMP'19 VeriFuzz*
- python-pandas *// SV-COMP'19 VeriFuzz*
- python-pycparser *// SV-COMP'19 CSeq*
- unzip *// SV-COMP'19 JBMC*

