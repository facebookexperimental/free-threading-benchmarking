# Results vs. 3.13.0rc2

- fork: python
- ref: 6ea3f8cd7ff4ff9769ae
- machine: linux-x86_64
- commit hash: 6ea3f8c
- commit date: 2026-01-27
- overall geometric mean: 1.041x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 248 ms: 1.05x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.56 sec: 1.02x faster                                                 |
| html5lib       | 67.0 ms                                                      | 59.7 ms: 1.12x faster                                                  |
| Geometric mean | (ref)                                                        | 1.06x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 564 ms: 1.62x faster                                                   |
| async_tree_io              | 876 ms                                                       | 552 ms: 1.59x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 302 ms: 1.53x faster                                                   |
| async_tree_none            | 354 ms                                                       | 244 ms: 1.45x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 293 ms: 1.41x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 246 ms: 1.37x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 490 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 492 ms: 1.29x faster                                                   |
| async_generators           | 377 ms                                                       | 341 ms: 1.11x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 23.9 ms: 1.01x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.31x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 70.9 ms: 1.09x faster                                                  |
| pidigits       | 217 ms                                                       | 202 ms: 1.07x faster                                                   |
| nbody          | 85.1 ms                                                      | 90.8 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.75 ms: 1.12x faster                                                  |
| regex_compile  | 132 ms                                                       | 123 ms: 1.08x faster                                                   |
| regex_dna      | 180 ms                                                       | 173 ms: 1.04x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 22.4 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                        | 1.06x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 84.4 ms: 1.12x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.82 sec: 1.10x faster                                                 |
| json_dumps           | 10.5 ms                                                      | 9.73 ms: 1.08x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 82.1 ms: 1.04x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 57.9 ms: 1.03x faster                                                  |
| unpickle_pure_python | 210 us                                                       | 213 us: 1.01x slower                                                   |
| json_loads           | 27.0 us                                                      | 28.1 us: 1.04x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 309 us: 1.05x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.28 ms: 1.01x faster                                                  |
| python_startup         | 11.0 ms                                                      | 12.5 ms: 1.13x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.06x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.8 ms: 1.01x slower                                                  |
| genshi_xml      | 48.8 ms                                                      | 49.9 ms: 1.02x slower                                                  |
| mako            | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                  |
| django_template | 34.1 ms                                                      | 35.7 ms: 1.05x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.03x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.16 sec: 2.04x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 564 ms: 1.62x faster                                                   |
| async_tree_io              | 876 ms                                                       | 552 ms: 1.59x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 302 ms: 1.53x faster                                                   |
| deepcopy                   | 355 us                                                       | 238 us: 1.50x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 26.5 us: 1.48x faster                                                  |
| async_tree_none            | 354 ms                                                       | 244 ms: 1.45x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 293 ms: 1.41x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 246 ms: 1.37x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 490 ms: 1.36x faster                                                   |
| go                         | 141 ms                                                       | 105 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 492 ms: 1.29x faster                                                   |
| scimark_sor                | 134 ms                                                       | 108 ms: 1.25x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.63 us: 1.18x faster                                                  |
| spectral_norm              | 111 ms                                                       | 95.5 ms: 1.16x faster                                                  |
| scimark_fft                | 349 ms                                                       | 306 ms: 1.14x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 84.4 ms: 1.12x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 59.7 ms: 1.12x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.75 ms: 1.12x faster                                                  |
| pylint                     | 317 ms                                                       | 283 ms: 1.12x faster                                                   |
| async_generators           | 377 ms                                                       | 341 ms: 1.11x faster                                                   |
| tomli_loads                | 2.01 sec                                                     | 1.82 sec: 1.10x faster                                                 |
| pathlib                    | 19.2 ms                                                      | 17.5 ms: 1.10x faster                                                  |
| float                      | 77.5 ms                                                      | 70.9 ms: 1.09x faster                                                  |
| pyflate                    | 449 ms                                                       | 413 ms: 1.09x faster                                                   |
| dulwich_log                | 74.8 ms                                                      | 69.0 ms: 1.08x faster                                                  |
| json_dumps                 | 10.5 ms                                                      | 9.73 ms: 1.08x faster                                                  |
| richards                   | 45.2 ms                                                      | 42.0 ms: 1.08x faster                                                  |
| regex_compile              | 132 ms                                                       | 123 ms: 1.08x faster                                                   |
| pidigits                   | 217 ms                                                       | 202 ms: 1.07x faster                                                   |
| richards_super             | 51.6 ms                                                      | 48.4 ms: 1.07x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.44 ms: 1.06x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.22 sec: 1.05x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 700 ms: 1.05x faster                                                   |
| 2to3                       | 260 ms                                                       | 248 ms: 1.05x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.43 sec: 1.05x faster                                                 |
| logging_simple             | 6.16 us                                                      | 5.89 us: 1.05x faster                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 62.5 ms: 1.05x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| generators                 | 28.8 ms                                                      | 27.6 ms: 1.04x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.56 us: 1.04x faster                                                  |
| sympy_integrate            | 19.8 ms                                                      | 19.0 ms: 1.04x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 82.1 ms: 1.04x faster                                                  |
| hexiom                     | 5.99 ms                                                      | 5.76 ms: 1.04x faster                                                  |
| regex_dna                  | 180 ms                                                       | 173 ms: 1.04x faster                                                   |
| pycparser                  | 1.12 sec                                                     | 1.08 sec: 1.03x faster                                                 |
| scimark_lu                 | 113 ms                                                       | 109 ms: 1.03x faster                                                   |
| chaos                      | 57.3 ms                                                      | 55.8 ms: 1.03x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 57.9 ms: 1.03x faster                                                  |
| thrift                     | 778 us                                                       | 760 us: 1.02x faster                                                   |
| coverage                   | 83.0 ms                                                      | 81.1 ms: 1.02x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.56 sec: 1.02x faster                                                 |
| comprehensions             | 16.5 us                                                      | 16.1 us: 1.02x faster                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.28 ms: 1.01x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 22.4 ms: 1.01x faster                                                  |
| meteor_contest             | 102 ms                                                       | 101 ms: 1.01x faster                                                   |
| raytrace                   | 253 ms                                                       | 250 ms: 1.01x faster                                                   |
| logging_silent             | 103 ns                                                       | 102 ns: 1.01x faster                                                   |
| typing_runtime_protocols   | 155 us                                                       | 156 us: 1.01x slower                                                   |
| sympy_str                  | 275 ms                                                       | 277 ms: 1.01x slower                                                   |
| sympy_sum                  | 156 ms                                                       | 157 ms: 1.01x slower                                                   |
| nqueens                    | 78.6 ms                                                      | 79.3 ms: 1.01x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 23.9 ms: 1.01x slower                                                  |
| genshi_text                | 21.5 ms                                                      | 21.8 ms: 1.01x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 213 us: 1.01x slower                                                   |
| sqlite_synth               | 2.21 us                                                      | 2.25 us: 1.02x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 69.4 ms: 1.02x slower                                                  |
| json                       | 4.93 ms                                                      | 5.04 ms: 1.02x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 49.9 ms: 1.02x slower                                                  |
| sympy_expand               | 457 ms                                                       | 469 ms: 1.03x slower                                                   |
| mako                       | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                  |
| fannkuch                   | 370 ms                                                       | 383 ms: 1.04x slower                                                   |
| json_loads                 | 27.0 us                                                      | 28.1 us: 1.04x slower                                                  |
| django_template            | 34.1 ms                                                      | 35.7 ms: 1.05x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 309 us: 1.05x slower                                                   |
| deltablue                  | 3.12 ms                                                      | 3.29 ms: 1.05x slower                                                  |
| nbody                      | 85.1 ms                                                      | 90.8 ms: 1.07x slower                                                  |
| python_startup             | 11.0 ms                                                      | 12.5 ms: 1.13x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.31 ms: 1.37x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.88 ms: 1.41x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.32 ms: 1.44x slower                                                  |
| telco                      | 7.82 ms                                                      | 158 ms: 20.25x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 279 ms: 25.36x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.00x slower                                                           |
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260127-3.15.0a5+-6ea3f8c/bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.041x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.15x