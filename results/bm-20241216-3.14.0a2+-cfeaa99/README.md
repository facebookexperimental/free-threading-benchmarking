# Results

- fork: python/cfeaa992ba9bad9be268
- version: 3.14.0a2+
- config: 
- commit hash: [cfeaa99](https://github.com/python/cpython/commit/cfeaa99)
- commit date: 2024-12-16T22:59:36+02:00
- commit merge base: [3b766824fe59030100964752be0556084d4461af](https://github.com/python/cpython/commit/3b766824fe59030100964752be0556084d4461af)
- ref: cfeaa992ba9bad9be268

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12363849799)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2%2B-cfeaa99.json)

### vs. 3.12.6

- Geometric mean: 1.118x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2%2B-cfeaa99-vs-3.12.6.md)
- [📈time plot](bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2%2B-cfeaa99-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.072x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2%2B-cfeaa99-vs-3.13.0rc2.md)
- [📈time plot](bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2%2B-cfeaa99-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12363849799)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241216-vultr-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2%2B-cfeaa99.json)

### vs. 3.12.6

- Geometric mean: 1.088x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241216-vultr-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2%2B-cfeaa99-vs-3.12.6.md)
- [📈time plot](bm-20241216-vultr-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2%2B-cfeaa99-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.049x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241216-vultr-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2%2B-cfeaa99-vs-3.13.0rc2.md)
- [📈time plot](bm-20241216-vultr-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2%2B-cfeaa99-vs-3.13.0rc2.svg)

