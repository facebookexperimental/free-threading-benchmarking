# Results

- fork: Fidget-Spinner/jit_Ft_llvm_19
- version: 3.15.0a1+
- config: JIT,NOGIL
- commit hash: [afae648](https://github.com/Fidget%2dSpinner/cpython/commit/afae648)
- commit date: 2025-11-16T20:20:52+00:00
- commit merge base: [ed73c909f278a1eb558b120ef8ed2c0f8528bf58](https://github.com/python/cpython/commit/ed73c909f278a1eb558b120ef8ed2c0f8528bf58)
- ref: jit_Ft_llvm_19

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19411477541)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251116-vultr-x86_64-Fidget%252dSpinner-jit_Ft_llvm_19-3.15.0a1%2B-afae648.json)

### vs. 3.12.6

- Geometric mean: 1.014x slower (HPT: reliability of 70.90%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, async_generators, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, docutils, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251116-vultr-x86_64-Fidget%252dSpinner-jit_Ft_llvm_19-3.15.0a1%2B-afae648-vs-3.12.6.md)
- [📈time plot](bm-20251116-vultr-x86_64-Fidget%252dSpinner-jit_Ft_llvm_19-3.15.0a1%2B-afae648-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.048x slower (HPT: reliability of 82.22%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, async_generators, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, docutils, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251116-vultr-x86_64-Fidget%252dSpinner-jit_Ft_llvm_19-3.15.0a1%2B-afae648-vs-3.13.0rc2.md)
- [📈time plot](bm-20251116-vultr-x86_64-Fidget%252dSpinner-jit_Ft_llvm_19-3.15.0a1%2B-afae648-vs-3.13.0rc2.svg)

