# Results

- fork: python/a3990df6121880e8c678
- version: 3.14.0a5+
- config: 
- commit hash: [a3990df](https://github.com/python/cpython/commit/a3990df)
- commit date: 2025-03-08T16:37:05-05:00
- commit merge base: [edd1eca336976b3431cf636aea87f08a40c94935](https://github.com/python/cpython/commit/edd1eca336976b3431cf636aea87f08a40c94935)
- ref: a3990df6121880e8c678

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13742756571)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [pystats raw](bm-20250308-linux-x86_64-python-a3990df6121880e8c678-3.14.0a5%2B-a3990df-pystats.json)
- [pystats table](bm-20250308-linux-x86_64-python-a3990df6121880e8c678-3.14.0a5%2B-a3990df-pystats.md)
- [raw results](bm-20250308-linux-x86_64-python-a3990df6121880e8c678-3.14.0a5%2B-a3990df.json)

### vs. 3.12.6

- Geometric mean: 1.107x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250308-linux-x86_64-python-a3990df6121880e8c678-3.14.0a5%2B-a3990df-vs-3.12.6.md)
- [📈time plot](bm-20250308-linux-x86_64-python-a3990df6121880e8c678-3.14.0a5%2B-a3990df-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.066x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250308-linux-x86_64-python-a3990df6121880e8c678-3.14.0a5%2B-a3990df-vs-3.13.0rc2.md)
- [📈time plot](bm-20250308-linux-x86_64-python-a3990df6121880e8c678-3.14.0a5%2B-a3990df-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13742756571)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250308-vultr-x86_64-python-a3990df6121880e8c678-3.14.0a5%2B-a3990df.json)

### vs. 3.12.6

- Geometric mean: 1.102x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250308-vultr-x86_64-python-a3990df6121880e8c678-3.14.0a5%2B-a3990df-vs-3.12.6.md)
- [📈time plot](bm-20250308-vultr-x86_64-python-a3990df6121880e8c678-3.14.0a5%2B-a3990df-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.061x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250308-vultr-x86_64-python-a3990df6121880e8c678-3.14.0a5%2B-a3990df-vs-3.13.0rc2.md)
- [📈time plot](bm-20250308-vultr-x86_64-python-a3990df6121880e8c678-3.14.0a5%2B-a3990df-vs-3.13.0rc2.svg)

