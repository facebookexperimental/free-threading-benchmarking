# Results

- fork: python/0cafa97932c6574734bb
- version: 3.14.0a3+
- config: 
- commit hash: [0cafa97](https://github.com/python/cpython/commit/0cafa97)
- commit date: 2025-01-04T23:38:46+00:00
- commit merge base: [e8b6b39ff707378da654e15ccddde9c28cefdd30](https://github.com/python/cpython/commit/e8b6b39ff707378da654e15ccddde9c28cefdd30)
- ref: 0cafa97932c6574734bb

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12614836491)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250104-linux-x86_64-python-0cafa97932c6574734bb-3.14.0a3%2B-0cafa97.json)

### vs. 3.12.6

- Geometric mean: 1.133x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250104-linux-x86_64-python-0cafa97932c6574734bb-3.14.0a3%2B-0cafa97-vs-3.12.6.md)
- [📈time plot](bm-20250104-linux-x86_64-python-0cafa97932c6574734bb-3.14.0a3%2B-0cafa97-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.086x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250104-linux-x86_64-python-0cafa97932c6574734bb-3.14.0a3%2B-0cafa97-vs-3.13.0rc2.md)
- [📈time plot](bm-20250104-linux-x86_64-python-0cafa97932c6574734bb-3.14.0a3%2B-0cafa97-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12614836491)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250104-vultr-x86_64-python-0cafa97932c6574734bb-3.14.0a3%2B-0cafa97.json)

### vs. 3.12.6

- Geometric mean: 1.088x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250104-vultr-x86_64-python-0cafa97932c6574734bb-3.14.0a3%2B-0cafa97-vs-3.12.6.md)
- [📈time plot](bm-20250104-vultr-x86_64-python-0cafa97932c6574734bb-3.14.0a3%2B-0cafa97-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.049x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250104-vultr-x86_64-python-0cafa97932c6574734bb-3.14.0a3%2B-0cafa97-vs-3.13.0rc2.md)
- [📈time plot](bm-20250104-vultr-x86_64-python-0cafa97932c6574734bb-3.14.0a3%2B-0cafa97-vs-3.13.0rc2.svg)

