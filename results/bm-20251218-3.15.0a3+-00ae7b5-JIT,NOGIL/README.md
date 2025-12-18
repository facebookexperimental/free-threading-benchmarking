# Results

- fork: Fidget-Spinner/jit_ft
- version: 3.15.0a3+
- config: JIT,NOGIL
- commit hash: [00ae7b5](https://github.com/Fidget%2dSpinner/cpython/commit/00ae7b5)
- commit date: 2025-12-18T01:07:08+00:00
- commit merge base: [8b64dd853ded593e1f0c5df786f1f1cc74dc7239](https://github.com/python/cpython/commit/8b64dd853ded593e1f0c5df786f1f1cc74dc7239)
- ref: jit_ft

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20322471512)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251218-vultr-x86_64-Fidget%252dSpinner-jit_ft-3.15.0a3%2B-00ae7b5.json)

### vs. 3.12.6

- Geometric mean: 1.003x faster (HPT: reliability of 64.41%, 1.00x faster at 99th %ile)
- Memory usage: 1.44x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251218-vultr-x86_64-Fidget%252dSpinner-jit_ft-3.15.0a3%2B-00ae7b5-vs-3.12.6.md)
- [📈time plot](bm-20251218-vultr-x86_64-Fidget%252dSpinner-jit_ft-3.15.0a3%2B-00ae7b5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.030x slower (HPT: reliability of 58.36%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251218-vultr-x86_64-Fidget%252dSpinner-jit_ft-3.15.0a3%2B-00ae7b5-vs-3.13.0rc2.md)
- [📈time plot](bm-20251218-vultr-x86_64-Fidget%252dSpinner-jit_ft-3.15.0a3%2B-00ae7b5-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.034x faster (HPT: reliability of 51.52%, 1.00x faster at 99th %ile)
- Memory usage: 1.03x
- [🧠memory plot](bm-20251218-vultr-x86_64-Fidget%252dSpinner-jit_ft-3.15.0a3%2B-00ae7b5-vs-base-mem.svg)
- [📄table](bm-20251218-vultr-x86_64-Fidget%252dSpinner-jit_ft-3.15.0a3%2B-00ae7b5-vs-base.md)
- [📈time plot](bm-20251218-vultr-x86_64-Fidget%252dSpinner-jit_ft-3.15.0a3%2B-00ae7b5-vs-base.svg)

