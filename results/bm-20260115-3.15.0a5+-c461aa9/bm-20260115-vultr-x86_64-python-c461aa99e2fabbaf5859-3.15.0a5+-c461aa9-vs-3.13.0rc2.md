# Results vs. 3.13.0rc2

- fork: python
- ref: c461aa99e2fabbaf5859
- machine: linux-x86_64
- commit hash: c461aa9
- commit date: 2026-01-15
- overall geometric mean: 1.038x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 249 ms: 1.04x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.57 sec: 1.02x faster                                                 |
| html5lib       | 67.0 ms                                                      | 59.2 ms: 1.13x faster                                                  |
| Geometric mean | (ref)                                                        | 1.06x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 554 ms: 1.58x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 587 ms: 1.56x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 306 ms: 1.51x faster                                                   |
| async_tree_none            | 354 ms                                                       | 243 ms: 1.45x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 477 ms: 1.40x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 243 ms: 1.38x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 305 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 478 ms: 1.33x faster                                                   |
| async_generators           | 377 ms                                                       | 338 ms: 1.12x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 24.4 ms: 1.04x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.04x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.31x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 197 ms: 1.10x faster                                                   |
| float          | 77.5 ms                                                      | 71.1 ms: 1.09x faster                                                  |
| nbody          | 85.1 ms                                                      | 91.4 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 132 ms                                                       | 124 ms: 1.07x faster                                                   |
| regex_effbot   | 3.08 ms                                                      | 2.91 ms: 1.06x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 22.2 ms: 1.02x faster                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 84.9 ms: 1.12x faster                                                  |
| json_dumps           | 10.5 ms                                                      | 9.58 ms: 1.10x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.86 sec: 1.08x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 82.6 ms: 1.03x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 58.2 ms: 1.02x faster                                                  |
| unpickle_pure_python | 210 us                                                       | 213 us: 1.02x slower                                                   |
| json_loads           | 27.0 us                                                      | 28.2 us: 1.04x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 310 us: 1.05x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.28 ms: 1.01x faster                                                  |
| python_startup         | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.06x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 49.7 ms: 1.02x slower                                                  |
| django_template | 34.1 ms                                                      | 35.6 ms: 1.04x slower                                                  |
| mako            | 11.3 ms                                                      | 12.1 ms: 1.06x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.03x slower                                                           |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.16 sec: 2.02x faster                                                 |
| async_tree_io              | 876 ms                                                       | 554 ms: 1.58x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 587 ms: 1.56x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 306 ms: 1.51x faster                                                   |
| deepcopy                   | 355 us                                                       | 238 us: 1.50x faster                                                   |
| async_tree_none            | 354 ms                                                       | 243 ms: 1.45x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 26.9 us: 1.45x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 477 ms: 1.40x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 243 ms: 1.38x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 305 ms: 1.36x faster                                                   |
| go                         | 141 ms                                                       | 105 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 478 ms: 1.33x faster                                                   |
| scimark_sor                | 134 ms                                                       | 106 ms: 1.27x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.59 us: 1.20x faster                                                  |
| spectral_norm              | 111 ms                                                       | 96.0 ms: 1.16x faster                                                  |
| scimark_fft                | 349 ms                                                       | 305 ms: 1.15x faster                                                   |
| html5lib                   | 67.0 ms                                                      | 59.2 ms: 1.13x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 84.9 ms: 1.12x faster                                                  |
| async_generators           | 377 ms                                                       | 338 ms: 1.12x faster                                                   |
| pylint                     | 317 ms                                                       | 285 ms: 1.11x faster                                                   |
| dulwich_log                | 74.8 ms                                                      | 67.6 ms: 1.11x faster                                                  |
| json_dumps                 | 10.5 ms                                                      | 9.58 ms: 1.10x faster                                                  |
| pidigits                   | 217 ms                                                       | 197 ms: 1.10x faster                                                   |
| pyflate                    | 449 ms                                                       | 409 ms: 1.10x faster                                                   |
| float                      | 77.5 ms                                                      | 71.1 ms: 1.09x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.6 ms: 1.09x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.86 sec: 1.08x faster                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.37 ms: 1.08x faster                                                  |
| regex_compile              | 132 ms                                                       | 124 ms: 1.07x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.91 ms: 1.06x faster                                                  |
| hexiom                     | 5.99 ms                                                      | 5.65 ms: 1.06x faster                                                  |
| richards_super             | 51.6 ms                                                      | 48.8 ms: 1.06x faster                                                  |
| richards                   | 45.2 ms                                                      | 42.8 ms: 1.06x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.21 sec: 1.06x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 702 ms: 1.05x faster                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 62.2 ms: 1.05x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.43 sec: 1.05x faster                                                 |
| 2to3                       | 260 ms                                                       | 249 ms: 1.04x faster                                                   |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| logging_simple             | 6.16 us                                                      | 5.92 us: 1.04x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.59 us: 1.04x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 109 ms: 1.04x faster                                                   |
| sympy_integrate            | 19.8 ms                                                      | 19.2 ms: 1.03x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 82.6 ms: 1.03x faster                                                  |
| generators                 | 28.8 ms                                                      | 28.0 ms: 1.03x faster                                                  |
| comprehensions             | 16.5 us                                                      | 16.0 us: 1.03x faster                                                  |
| chaos                      | 57.3 ms                                                      | 55.9 ms: 1.03x faster                                                  |
| pycparser                  | 1.12 sec                                                     | 1.09 sec: 1.02x faster                                                 |
| xml_etree_process          | 59.3 ms                                                      | 58.2 ms: 1.02x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 22.2 ms: 1.02x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.57 sec: 1.02x faster                                                 |
| coverage                   | 83.0 ms                                                      | 81.5 ms: 1.02x faster                                                  |
| logging_silent             | 103 ns                                                       | 101 ns: 1.01x faster                                                   |
| python_startup_no_site     | 7.39 ms                                                      | 7.28 ms: 1.01x faster                                                  |
| thrift                     | 778 us                                                       | 768 us: 1.01x faster                                                   |
| meteor_contest             | 102 ms                                                       | 101 ms: 1.01x faster                                                   |
| sympy_sum                  | 156 ms                                                       | 156 ms: 1.00x slower                                                   |
| nqueens                    | 78.6 ms                                                      | 79.2 ms: 1.01x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 213 us: 1.02x slower                                                   |
| sympy_str                  | 275 ms                                                       | 280 ms: 1.02x slower                                                   |
| genshi_xml                 | 48.8 ms                                                      | 49.7 ms: 1.02x slower                                                  |
| json                       | 4.93 ms                                                      | 5.04 ms: 1.02x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 158 us: 1.02x slower                                                   |
| crypto_pyaes               | 67.9 ms                                                      | 69.7 ms: 1.03x slower                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.28 us: 1.03x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 24.4 ms: 1.04x slower                                                  |
| django_template            | 34.1 ms                                                      | 35.6 ms: 1.04x slower                                                  |
| json_loads                 | 27.0 us                                                      | 28.2 us: 1.04x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.04x slower                                                   |
| fannkuch                   | 370 ms                                                       | 388 ms: 1.05x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 310 us: 1.05x slower                                                   |
| mako                       | 11.3 ms                                                      | 12.1 ms: 1.06x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.32 ms: 1.06x slower                                                  |
| nbody                      | 85.1 ms                                                      | 91.4 ms: 1.07x slower                                                  |
| sympy_expand               | 457 ms                                                       | 491 ms: 1.08x slower                                                   |
| python_startup             | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.00 ms: 1.27x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.86 ms: 1.39x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.31 ms: 1.43x slower                                                  |
| telco                      | 7.82 ms                                                      | 160 ms: 20.40x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 283 ms: 25.70x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (3): regex_dna, raytrace, genshi_text
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260115-3.15.0a5+-c461aa9/bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.038x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.15x