# Results

- fork: mpage
- version: 3.14.0a0
- config: NOGIL
- commit hash: [f483286](https://github.com/mpage/cpython/commit/f483286)
- commit date: 2024-08-07T16:04:26-07:00
- commit merge base: [e006c7371d8e57db26254792c67292956e88d81d](https://github.com/mpage/cpython/commit/e006c7371d8e57db26254792c67292956e88d81d)
- ref: gh_122712_fix_call_a

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10306123426)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286.json)

### vs. 3.12.6

- Geometric mean: 1.38x slower (HPT: reliability of 100.00%, 1.27x slower at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286-vs-3.12.6.md)
- [📈time plot](bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.43x slower (HPT: reliability of 100.00%, 1.31x slower at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn
- [📄table](bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286-vs-3.13.0rc2.md)
- [📈time plot](bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.00x slower (HPT: reliability of 76.87%, 1.00x faster at 99th %ile)
- Memory usage: 0.99x
- [🧠memory plot](bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286-vs-base-mem.svg)
- [📄table](bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286-vs-base.md)
- [📈time plot](bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.45x slower (HPT: reliability of 100.00%, 1.31x slower at 99th %ile)
- Memory usage: 1.14x
- [📄table](bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286-vs-default_base_vs_NOGIL.svg)

### vs. 3.12.0b1

- [📄table](bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286-vs-3.12.0b1.md)
- [📈time plot](bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286-vs-3.12.0b1.svg)

### vs. 3.12.5+

- [📄table](bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286-vs-3.12.5%2B.md)
- [📈time plot](bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286-vs-3.12.5%2B.svg)

### vs. 3.13.0b1

- [📄table](bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286-vs-3.13.0b1.md)
- [📈time plot](bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286-vs-3.13.0b1.svg)

### vs. 3.13.0rc1+

- [📄table](bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286-vs-3.13.0rc1%2B.md)
- [📈time plot](bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286-vs-3.13.0rc1%2B.svg)

