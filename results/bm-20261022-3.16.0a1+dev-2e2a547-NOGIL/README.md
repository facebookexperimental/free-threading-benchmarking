# Results

- fork: corona10/MI_SEGMENT_SLICE_SHI
- version: 3.16.0a1+dev
- config: NOGIL
- commit hash: [2e2a547](https://github.com/corona10/cpython/commit/2e2a547)
- commit date: 2026-10-22T14:48:26-07:00
- commit merge base: [5b55b502221b67660a4d652cdd3dd2203920e58a](https://github.com/python/cpython/commit/5b55b502221b67660a4d652cdd3dd2203920e58a)
- ref: MI_SEGMENT_SLICE_SHI

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/39860993693)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261022-vultr-x86_64-corona10-MI_SEGMENT_SLICE_SHI-3.16.0a1%2Bdev-2e2a547.json)

### vs. 3.12.6

- Geometric mean: 1.033x slower (HPT: reliability of 73.57%, 1.00x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261022-vultr-x86_64-corona10-MI_SEGMENT_SLICE_SHI-3.16.0a1%2Bdev-2e2a547-vs-3.12.6.md)
- [📈time plot](bm-20261022-vultr-x86_64-corona10-MI_SEGMENT_SLICE_SHI-3.16.0a1%2Bdev-2e2a547-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.066x slower (HPT: reliability of 90.02%, 1.00x slower at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261022-vultr-x86_64-corona10-MI_SEGMENT_SLICE_SHI-3.16.0a1%2Bdev-2e2a547-vs-3.13.0rc2.md)
- [📈time plot](bm-20261022-vultr-x86_64-corona10-MI_SEGMENT_SLICE_SHI-3.16.0a1%2Bdev-2e2a547-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.004x faster (HPT: reliability of 64.60%, 1.00x faster at 99th %ile)
- Memory usage: 0.97x
- [🧠memory plot](bm-20261022-vultr-x86_64-corona10-MI_SEGMENT_SLICE_SHI-3.16.0a1%2Bdev-2e2a547-vs-base-mem.svg)
- [📄table](bm-20261022-vultr-x86_64-corona10-MI_SEGMENT_SLICE_SHI-3.16.0a1%2Bdev-2e2a547-vs-base.md)
- [📈time plot](bm-20261022-vultr-x86_64-corona10-MI_SEGMENT_SLICE_SHI-3.16.0a1%2Bdev-2e2a547-vs-base.svg)

