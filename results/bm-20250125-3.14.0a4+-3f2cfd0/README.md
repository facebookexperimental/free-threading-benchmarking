# Results

- fork: python/3f2cfd0462e13368092a
- version: 3.14.0a4+
- config: 
- commit hash: [3f2cfd0](https://github.com/python/cpython/commit/3f2cfd0)
- commit date: 2025-01-25T23:50:09+05:30
- commit merge base: [be98fda7c6698e8468afd528c864aca1f532af59](https://github.com/python/cpython/commit/be98fda7c6698e8468afd528c864aca1f532af59)
- ref: 3f2cfd0462e13368092a

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12969596525)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [pystats raw](bm-20250125-linux-x86_64-python-3f2cfd0462e13368092a-3.14.0a4%2B-3f2cfd0-pystats.json)
- [pystats table](bm-20250125-linux-x86_64-python-3f2cfd0462e13368092a-3.14.0a4%2B-3f2cfd0-pystats.md)
- [raw results](bm-20250125-linux-x86_64-python-3f2cfd0462e13368092a-3.14.0a4%2B-3f2cfd0.json)

### vs. 3.12.6

- Geometric mean: 1.072x faster (HPT: reliability of 99.99%, 1.02x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250125-linux-x86_64-python-3f2cfd0462e13368092a-3.14.0a4%2B-3f2cfd0-vs-3.12.6.md)
- [📈time plot](bm-20250125-linux-x86_64-python-3f2cfd0462e13368092a-3.14.0a4%2B-3f2cfd0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.030x faster (HPT: reliability of 99.95%, 1.01x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250125-linux-x86_64-python-3f2cfd0462e13368092a-3.14.0a4%2B-3f2cfd0-vs-3.13.0rc2.md)
- [📈time plot](bm-20250125-linux-x86_64-python-3f2cfd0462e13368092a-3.14.0a4%2B-3f2cfd0-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12969596525)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250125-vultr-x86_64-python-3f2cfd0462e13368092a-3.14.0a4%2B-3f2cfd0.json)

### vs. 3.12.6

- Geometric mean: 1.088x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250125-vultr-x86_64-python-3f2cfd0462e13368092a-3.14.0a4%2B-3f2cfd0-vs-3.12.6.md)
- [📈time plot](bm-20250125-vultr-x86_64-python-3f2cfd0462e13368092a-3.14.0a4%2B-3f2cfd0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.050x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250125-vultr-x86_64-python-3f2cfd0462e13368092a-3.14.0a4%2B-3f2cfd0-vs-3.13.0rc2.md)
- [📈time plot](bm-20250125-vultr-x86_64-python-3f2cfd0462e13368092a-3.14.0a4%2B-3f2cfd0-vs-3.13.0rc2.svg)

