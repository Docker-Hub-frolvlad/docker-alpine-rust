[![Docker Stars](https://img.shields.io/docker/stars/frolvlad/alpine-rust.svg?style=flat-square)](https://hub.docker.com/r/frolvlad/alpine-rust/)
[![Docker Pulls](https://img.shields.io/docker/pulls/frolvlad/alpine-rust.svg?style=flat-square)](https://hub.docker.com/r/frolvlad/alpine-rust/)


Rust Docker image
=================

This image is based on Alpine Linux image, which is only a 5MB image, and contains
[Rust](https://www.rust-lang.org/) with [GCC](https://gcc.gnu.org/).

This image download size is:

[![](https://badge.imagelayers.io/frolvlad/alpine-rust.svg)](https://imagelayers.io/?images=frolvlad/alpine-rust 'Get your own badge on imagelayers.io')


Usage Example
-------------

```bash
$ echo -e 'fn main() { println!("Hello world"); }' > qq.rs
$ docker run --rm -v "$(pwd):/tmp" --workdir /tmp frolvlad/alpine-rust rustc -C target-feature=+crt-static ./qq.rs
```

Once you have run these commands you will have `qq` executable in your current directory and if you
execute it, you will get printed 'Hello World'!
