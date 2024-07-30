# Introduction

This Package forms part of the seL4 Developer Kit. It provides a fully
coordinated build of the MaaXBoard CAmkES adder example.

Its main purpose is to confirm first boot, demonstrating that the overall
environment is functioning as intended.

# Usage

Must be invoked inside the following:
* sel4devkit-maaxboard-camkes-docker-dev-env

Show usage instructions:
```
make
```

Build program:
```
make all
```
Expected output where executed on target:
```
u-boot=> bootelf 0x50000000
## Starting application at 0x4085e000 ...

ELF-loader started on CPU: ARM Ltd. Cortex-A53 r0p4
  paddr=[4085e000..40b6d137]
No DTB passed in from boot loader.
Looking for DTB in CPIO archive...found at 409a0a08.
Loaded DTB from 409a0a08.
   paddr=[4023f000..40249fff]
ELF-loading image 'kernel' to 40000000
  paddr=[40000000..4023efff]
  vaddr=[ffffff8040000000..ffffff804023efff]
  virt_entry=ffffff8040000000
ELF-loading image 'capdl-loader' to 4024a000
  paddr=[4024a000..40462fff]
  vaddr=[400000..618fff]
  virt_entry=408e98
Enabling MMU and paging
Jumping to kernel-image entry point...

Warning:  gpt_cntfrq 8333333, expected 8000000
Bootstrapping kernel
available phys memory regions: 1
  [40000000..c0000000]
reserved virt address space regions: 3
  [ffffff8040000000..ffffff804023f000]
  [ffffff804023f000..ffffff80402492c7]
  [ffffff804024a000..ffffff8040463000]
Booting all finished, dropped to user space
client: what's the answer to 342 + 74 + 283 + 37 + 534 ?
adder: Adding 342
adder: Adding 74
adder: Adding 283
adder: Adding 37
adder: Adding 534
client: result was 1270
```
