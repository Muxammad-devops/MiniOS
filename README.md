miniOS — a minimal x86_64 hobby operating system

miniOS is a small, educational operating system built from scratch for the x86_64 architecture.
The project is focused on understanding how a system boots, how a kernel is loaded by GRUB (Multiboot2), and how low-level components work together in a freestanding environment.

This repository is part of my learning journey in operating system development and low-level systems programming.

What’s inside

GRUB (Multiboot2) boot support

Freestanding C kernel (no libc, no host OS dependencies)

Basic VGA text output

Bootable ISO image

QEMU support for local testing

Build & run

Linux / WSL:

make run


Docker (no toolchain setup required):

./scripts/docker-toolchain.sh


This builds the kernel, creates a bootable ISO, and starts QEMU.

Project structure
minios/
├─ kernel/        # kernel sources
├─ arch/x86_64/   # boot + linker
├─ iso/           # GRUB config for ISO
├─ scripts/       # helper scripts
├─ .github/       # CI
├─ Makefile

Roadmap

Improve VGA text handling (scrolling, cursor)

Add interrupts (IDT)

Keyboard input

Simple shell
