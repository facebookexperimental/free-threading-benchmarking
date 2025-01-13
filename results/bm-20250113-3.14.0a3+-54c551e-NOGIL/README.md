# Results

- fork: Yhg1s/for_iter_spec
- version: 3.14.0a3+
- config: NOGIL
- commit hash: [54c551e](https://github.com/Yhg1s/cpython/commit/54c551e)
- commit date: 2025-01-13T01:59:30+01:00
- commit merge base: [7dc41ad6a7826ffc675f088972de96624917696e](https://github.com/python/cpython/commit/7dc41ad6a7826ffc675f088972de96624917696e)
- ref: for_iter_spec

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12738766432)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3%2B-54c551e.json)

### vs. 3.12.6

- Geometric mean: 1.165x slower (HPT: reliability of 100.00%, 1.14x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3%2B-54c551e-vs-3.12.6.md)
- [📈time plot](bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3%2B-54c551e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.194x slower (HPT: reliability of 100.00%, 1.17x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3%2B-54c551e-vs-3.13.0rc2.md)
- [📈time plot](bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3%2B-54c551e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.012x slower (HPT: reliability of 99.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3%2B-54c551e-vs-base-mem.svg)
- [📄table](bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3%2B-54c551e-vs-base.md)
- [📈time plot](bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3%2B-54c551e-vs-base.svg)

