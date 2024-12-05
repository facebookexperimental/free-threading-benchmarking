# Results

- fork: mpage/3ff07d95fb0878c32376
- version: 3.13.0rc2
- config: 
- commit hash: [3ff07d9](https://github.com/mpage/cpython/commit/3ff07d9)
- commit date: 2024-09-20T20:20:28-07:00
- ref: 3ff07d95fb0878c32376

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10970085987)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20240920-linux-x86_64-mpage-3ff07d95fb0878c32376-3.13.0rc2-3ff07d9.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 99.95%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- missing benchmarks: mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240920-linux-x86_64-mpage-3ff07d95fb0878c32376-3.13.0rc2-3ff07d9-vs-3.12.6.md)
- [📈time plot](bm-20240920-linux-x86_64-mpage-3ff07d95fb0878c32376-3.13.0rc2-3ff07d9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 77.22%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [📄table](bm-20240920-linux-x86_64-mpage-3ff07d95fb0878c32376-3.13.0rc2-3ff07d9-vs-3.13.0rc2.md)
- [📈time plot](bm-20240920-linux-x86_64-mpage-3ff07d95fb0878c32376-3.13.0rc2-3ff07d9-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10969279865)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20240920-vultr-x86_64-mpage-3ff07d95fb0878c32376-3.13.0rc2-3ff07d9.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- missing benchmarks: mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240920-vultr-x86_64-mpage-3ff07d95fb0878c32376-3.13.0rc2-3ff07d9-vs-3.12.6.md)
- [📈time plot](bm-20240920-vultr-x86_64-mpage-3ff07d95fb0878c32376-3.13.0rc2-3ff07d9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 69.23%, 1.00x slower at 99th %ile)
- Memory usage: 0.99x
- [📄table](bm-20240920-vultr-x86_64-mpage-3ff07d95fb0878c32376-3.13.0rc2-3ff07d9-vs-3.13.0rc2.md)
- [📈time plot](bm-20240920-vultr-x86_64-mpage-3ff07d95fb0878c32376-3.13.0rc2-3ff07d9-vs-3.13.0rc2.svg)

