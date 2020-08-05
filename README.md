# P4 dataplane program examples

This repository contains Proof-of-Concept P4 code related to a proposed design for an open source P4vSwitch implementation.

Building a P4 based BPF application using p4c-xdp + CLANG + BPF CO-RE consists of few steps:

    offline generation of vmlinux.h header file with all kernel types (stored in /lib/vmlinux.h);
    compiling your P4 program to a C based BPF program source code + p4runtime file using the p4c compiler with p4vswitch & ebpf & xdp extentions
    compiling your BPF program source code using recent Clang (version 10 or newer) into ELF based object file;
    then, at last, using the p4vswitch deamon with p4runtime GRPC api or the p4vswitch Go library in your VNF program.

How exactly this is done will depend on your specific setup and build system, which can’t be addressed here in enough details at this moment but will be added later on. 


