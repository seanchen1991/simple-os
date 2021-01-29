# Simple OS 

A freestanding Rust binary upon which OS abstractions can be built on top of.

## Initial Setup

1. Fork the repo, then clone it onto your local machine.
2. Download and install [QEMU][qemu-download], which is the virtual environment 
we'll be running our OS in.
3. `cd` into the root of the `simple-os` project and run `cargo test`. The 
output should include, among other things, five passing tests that look like the 
following:

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
