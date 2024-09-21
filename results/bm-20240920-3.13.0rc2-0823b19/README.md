# Results

- fork: mpage
- version: 3.13.0rc2
- config: 
- commit hash: [0823b19](https://github.com/mpage/cpython/commit/0823b19)
- commit date: 2024-09-20T20:20:16-07:00
- ref: 0823b19f44e0e8c6ef20

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10970084815)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20240920-linux-x86_64-mpage-0823b19f44e0e8c6ef20-3.13.0rc2-0823b19.json)

### vs. 3.12.6

- Geometric mean: 1.03x faster (HPT: reliability of 97.07%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- missing benchmarks: mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240920-linux-x86_64-mpage-0823b19f44e0e8c6ef20-3.13.0rc2-0823b19-vs-3.12.6.md)
- [📈time plot](bm-20240920-linux-x86_64-mpage-0823b19f44e0e8c6ef20-3.13.0rc2-0823b19-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.01x slower (HPT: reliability of 95.94%, 1.00x slower at 99th %ile)
- Memory usage: 0.98x
- [📄table](bm-20240920-linux-x86_64-mpage-0823b19f44e0e8c6ef20-3.13.0rc2-0823b19-vs-3.13.0rc2.md)
- [📈time plot](bm-20240920-linux-x86_64-mpage-0823b19f44e0e8c6ef20-3.13.0rc2-0823b19-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10969277897)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20240920-vultr-x86_64-mpage-0823b19f44e0e8c6ef20-3.13.0rc2-0823b19.json)

### vs. 3.12.6

- Geometric mean: 1.03x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240920-vultr-x86_64-mpage-0823b19f44e0e8c6ef20-3.13.0rc2-0823b19-vs-3.12.6.md)
- [📈time plot](bm-20240920-vultr-x86_64-mpage-0823b19f44e0e8c6ef20-3.13.0rc2-0823b19-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.00x faster (HPT: reliability of 92.18%, 1.00x slower at 99th %ile)
- Memory usage: 1.01x
- [📄table](bm-20240920-vultr-x86_64-mpage-0823b19f44e0e8c6ef20-3.13.0rc2-0823b19-vs-3.13.0rc2.md)
- [📈time plot](bm-20240920-vultr-x86_64-mpage-0823b19f44e0e8c6ef20-3.13.0rc2-0823b19-vs-3.13.0rc2.svg)

