# Results

- fork: python/ebc24d54bcf554403e9b
- version: 3.14.0a5+
- config: 
- commit hash: [ebc24d5](https://github.com/python/cpython/commit/ebc24d5)
- commit date: 2025-03-11T23:17:58+00:00
- commit merge base: [c00ac578241b3213ceb79c1f32bc83ea471f02da](https://github.com/python/cpython/commit/c00ac578241b3213ceb79c1f32bc83ea471f02da)
- ref: ebc24d54bcf554403e9b

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13800893559)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250311-vultr-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5.json)

### vs. 3.12.6

- Geometric mean: 1.053x faster (HPT: reliability of 99.96%, 1.00x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250311-vultr-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-3.12.6.md)
- [📈time plot](bm-20250311-vultr-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.014x faster (HPT: reliability of 58.98%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250311-vultr-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-3.13.0rc2.md)
- [📈time plot](bm-20250311-vultr-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-3.13.0rc2.svg)

