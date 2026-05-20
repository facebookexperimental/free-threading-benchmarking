# Results vs. 3.13.0rc2

- fork: python
- ref: de9c32fc34fe2e000de1
- machine: linux-x86_64
- commit hash: de9c32f
- commit date: 2026-05-20
- overall geometric mean: 1.024x faster
- HPT reliability: 99.71%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 2.62 sec                                                     | 2.40 sec: 1.09x faster                                                |
| html5lib       | 67.0 ms                                                      | 61.0 ms: 1.10x faster                                                 |
| Geometric mean | (ref)                                                        | 1.09x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 666 ms                                                       | 545 ms: 1.22x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 378 ms: 1.22x faster                                                  |
| async_tree_io              | 876 ms                                                       | 724 ms: 1.21x faster                                                  |
| async_tree_none            | 354 ms                                                       | 294 ms: 1.20x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 765 ms: 1.19x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 559 ms: 1.14x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 368 ms: 1.13x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 301 ms: 1.12x faster                                                  |
| async_generators           | 377 ms                                                       | 345 ms: 1.09x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 24.5 ms: 1.04x slower                                                 |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.13x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 192 ms: 1.13x faster                                                  |
| float          | 77.5 ms                                                      | 75.6 ms: 1.02x faster                                                 |
| nbody          | 85.1 ms                                                      | 90.5 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                        | 1.03x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.91 ms: 1.06x faster                                                 |
| regex_compile  | 132 ms                                                       | 126 ms: 1.05x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 21.9 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                        | 1.04x faster                                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.83 sec: 1.09x faster                                                |
| json_dumps           | 10.5 ms                                                      | 9.88 ms: 1.07x faster                                                 |
| xml_etree_iterparse  | 94.9 ms                                                      | 89.6 ms: 1.06x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 86.9 ms: 1.02x slower                                                 |
| json_loads           | 27.0 us                                                      | 27.7 us: 1.02x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 216 us: 1.03x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 61.4 ms: 1.03x slower                                                 |
| xml_etree_parse      | 136 ms                                                       | 142 ms: 1.05x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 317 us: 1.08x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.00x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 35.5 ms: 1.04x slower                                                 |
| mako            | 11.3 ms                                                      | 12.3 ms: 1.08x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.06x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 115 ms: 2.77x faster                                                  |
| mdp                        | 2.36 sec                                                     | 1.14 sec: 2.06x faster                                                |
| deepcopy                   | 355 us                                                       | 239 us: 1.49x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 27.5 us: 1.42x faster                                                 |
| typing_runtime_protocols   | 155 us                                                       | 118 us: 1.31x faster                                                  |
| go                         | 141 ms                                                       | 108 ms: 1.30x faster                                                  |
| scimark_sor                | 134 ms                                                       | 109 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 545 ms: 1.22x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 378 ms: 1.22x faster                                                  |
| async_tree_io              | 876 ms                                                       | 724 ms: 1.21x faster                                                  |
| async_tree_none            | 354 ms                                                       | 294 ms: 1.20x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.59 us: 1.20x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 765 ms: 1.19x faster                                                  |
| spectral_norm              | 111 ms                                                       | 96.2 ms: 1.15x faster                                                 |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 559 ms: 1.14x faster                                                  |
| pidigits                   | 217 ms                                                       | 192 ms: 1.13x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 368 ms: 1.13x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 301 ms: 1.12x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 61.0 ms: 1.10x faster                                                 |
| pyflate                    | 449 ms                                                       | 409 ms: 1.10x faster                                                  |
| scimark_fft                | 349 ms                                                       | 319 ms: 1.09x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.83 sec: 1.09x faster                                                |
| async_generators           | 377 ms                                                       | 345 ms: 1.09x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.6 ms: 1.09x faster                                                 |
| docutils                   | 2.62 sec                                                     | 2.40 sec: 1.09x faster                                                |
| dulwich_log                | 74.8 ms                                                      | 69.7 ms: 1.07x faster                                                 |
| json_dumps                 | 10.5 ms                                                      | 9.88 ms: 1.07x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 89.6 ms: 1.06x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.91 ms: 1.06x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.20 sec: 1.06x faster                                                |
| regex_compile              | 132 ms                                                       | 126 ms: 1.05x faster                                                  |
| nqueens                    | 78.6 ms                                                      | 75.4 ms: 1.04x faster                                                 |
| logging_silent             | 103 ns                                                       | 98.6 ns: 1.04x faster                                                 |
| regex_v8                   | 22.7 ms                                                      | 21.9 ms: 1.04x faster                                                 |
| sympy_integrate            | 19.8 ms                                                      | 19.2 ms: 1.03x faster                                                 |
| richards_super             | 51.6 ms                                                      | 50.0 ms: 1.03x faster                                                 |
| logging_simple             | 6.16 us                                                      | 5.96 us: 1.03x faster                                                 |
| richards                   | 45.2 ms                                                      | 43.8 ms: 1.03x faster                                                 |
| meteor_contest             | 102 ms                                                       | 98.7 ms: 1.03x faster                                                 |
| chaos                      | 57.3 ms                                                      | 55.7 ms: 1.03x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.84 ms: 1.03x faster                                                 |
| float                      | 77.5 ms                                                      | 75.6 ms: 1.02x faster                                                 |
| comprehensions             | 16.5 us                                                      | 16.1 us: 1.02x faster                                                 |
| logging_format             | 6.84 us                                                      | 6.69 us: 1.02x faster                                                 |
| pycparser                  | 1.12 sec                                                     | 1.11 sec: 1.01x faster                                                |
| scimark_monte_carlo        | 65.4 ms                                                      | 65.0 ms: 1.01x faster                                                 |
| generators                 | 28.8 ms                                                      | 29.2 ms: 1.01x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 86.9 ms: 1.02x slower                                                 |
| coverage                   | 83.0 ms                                                      | 84.6 ms: 1.02x slower                                                 |
| scimark_lu                 | 113 ms                                                       | 115 ms: 1.02x slower                                                  |
| json_loads                 | 27.0 us                                                      | 27.7 us: 1.02x slower                                                 |
| fannkuch                   | 370 ms                                                       | 379 ms: 1.02x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 216 us: 1.03x slower                                                  |
| thrift                     | 778 us                                                       | 801 us: 1.03x slower                                                  |
| raytrace                   | 253 ms                                                       | 261 ms: 1.03x slower                                                  |
| sympy_expand               | 457 ms                                                       | 472 ms: 1.03x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 61.4 ms: 1.03x slower                                                 |
| django_template            | 34.1 ms                                                      | 35.5 ms: 1.04x slower                                                 |
| coroutines                 | 23.6 ms                                                      | 24.5 ms: 1.04x slower                                                 |
| xml_etree_parse            | 136 ms                                                       | 142 ms: 1.05x slower                                                  |
| json                       | 4.93 ms                                                      | 5.15 ms: 1.05x slower                                                 |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 71.1 ms: 1.05x slower                                                 |
| nbody                      | 85.1 ms                                                      | 90.5 ms: 1.06x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 317 us: 1.08x slower                                                  |
| mako                       | 11.3 ms                                                      | 12.3 ms: 1.08x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.45 ms: 1.11x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.15 ms: 1.32x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.82 ms: 1.36x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.35 ms: 1.47x slower                                                 |
| telco                      | 7.82 ms                                                      | 161 ms: 20.58x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 243 ms: 22.06x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.02x slower                                                          |

Benchmark hidden because not significant (7): regex_dna, pprint_safe_repr, pprint_pformat, sympy_sum, sqlite_synth, sympy_str, scimark_sparse_mat_mult
Ignored benchmarks (23) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260520-3.16.0a0-de9c32f/bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.024x faster

# HPT report

- Reliability score: 99.71% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.16x