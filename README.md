# Simple OS 

A freestanding Rust binary upon which OS abstractions can be built on top of.

## Initial Setup

1. Make sure that you're running the `nightly` version of the Rust compiler. If
you're unsure, make sure you have [rustup][rustup-dowload] installed and then 
run `rustup toolchain install nightly` to install and switch to the `nightly`
toolchain.
2. Fork the repo, then clone it onto your local machine.
3. Download and install [QEMU][qemu-download], which is the virtual environment 
we'll be running our OS in.
4. `cd` into the root of the `simple-os` project.
5. We'll need to add Rust's `core` and `compiler_builtins` libraries locally. Do
this by running `rustup component add rust-src`. 
6. Run `cargo build` to see if everything compiles without issue.
7. Run `cargo test`. The output should include, among other things, five passing
tests that look like the following:

```
simple_os::vga_buffer::test_println_simple...   [ok]
simple_os::vga_buffer::test_println_many...   [ok]
simple_os::vga_buffer::test_println_output...   [ok]
simple_os::vga_buffer::test_println...   [ok]
should_panic::should_fail...   [ok]
```

If you see these statements in your `cargo test` output, then everything worked, 
and you should be good to go! If you see something different, reach out and let me know
so we can look into it.

[qemu-download]: https://www.qemu.org/download/#windows
