# Results vs. 3.12.6

- fork: faster-cpython
- ref: use_stackrefs
- machine: linux-x86_64
- commit hash: e2f1387
- commit date: 2025-03-03
- overall geometric mean: 1.043x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250303-vultr-x86_64-faster%2dcpython-use_stackrefs-3.14.0a5+-e2f1387 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 307 ms: 1.16x slower                                                      |
| docutils       | 2.64 sec                                               | 2.80 sec: 1.06x slower                                                    |
| html5lib       | 63.6 ms                                                | 70.6 ms: 1.11x slower                                                     |
| Geometric mean | (ref)                                                  | 1.11x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250303-vultr-x86_64-faster%2dcpython-use_stackrefs-3.14.0a5+-e2f1387 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 550 ms: 2.02x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 239 ms: 1.87x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 581 ms: 1.86x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 307 ms: 1.82x faster                                                      |
| async_tree_none            | 464 ms                                                 | 275 ms: 1.69x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 339 ms: 1.64x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 499 ms: 1.45x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 528 ms: 1.35x faster                                                      |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                     |
| async_generators           | 384 ms                                                 | 374 ms: 1.03x faster                                                      |
| Geometric mean             | (ref)                                                  | 1.48x faster                                                              |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250303-vultr-x86_64-faster%2dcpython-use_stackrefs-3.14.0a5+-e2f1387 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 77.0 ms: 1.05x faster                                                     |
| pidigits       | 184 ms                                                 | 191 ms: 1.04x slower                                                      |
| nbody          | 89.3 ms                                                | 131 ms: 1.46x slower                                                      |
| Geometric mean | (ref)                                                  | 1.13x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250303-vultr-x86_64-faster%2dcpython-use_stackrefs-3.14.0a5+-e2f1387 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.74 ms: 1.15x faster                                                     |
| regex_dna      | 168 ms                                                 | 170 ms: 1.02x slower                                                      |
| regex_compile  | 142 ms                                                 | 156 ms: 1.10x slower                                                      |
| regex_v8       | 20.6 ms                                                | 23.0 ms: 1.12x slower                                                     |
| Geometric mean | (ref)                                                  | 1.02x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250303-vultr-x86_64-faster%2dcpython-use_stackrefs-3.14.0a5+-e2f1387 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.6 ms: 1.10x faster                                                     |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                                      |
| tomli_loads          | 2.11 sec                                               | 2.33 sec: 1.10x slower                                                    |
| json_loads           | 26.5 us                                                | 29.3 us: 1.10x slower                                                     |
| xml_etree_generate   | 85.2 ms                                                | 95.5 ms: 1.12x slower                                                     |
| unpickle_pure_python | 221 us                                                 | 252 us: 1.14x slower                                                      |
| pickle_pure_python   | 308 us                                                 | 362 us: 1.18x slower                                                      |
| xml_etree_process    | 59.0 ms                                                | 69.7 ms: 1.18x slower                                                     |
| json_dumps           | 10.4 ms                                                | 12.7 ms: 1.23x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.09x slower                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250303-vultr-x86_64-faster%2dcpython-use_stackrefs-3.14.0a5+-e2f1387 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.68 ms: 1.35x slower                                                     |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                     |
| Geometric mean         | (ref)                                                  | 1.46x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250303-vultr-x86_64-faster%2dcpython-use_stackrefs-3.14.0a5+-e2f1387 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 60.1 ms: 1.20x slower                                                     |
| django_template | 34.7 ms                                                | 42.5 ms: 1.23x slower                                                     |
| genshi_text     | 22.8 ms                                                | 28.2 ms: 1.24x slower                                                     |
| mako            | 11.0 ms                                                | 16.0 ms: 1.45x slower                                                     |
| Geometric mean  | (ref)                                                  | 1.27x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250303-vultr-x86_64-faster%2dcpython-use_stackrefs-3.14.0a5+-e2f1387 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 1.70 ms: 2.04x faster                                                     |
| async_tree_io_tg           | 1.11 sec                                               | 550 ms: 2.02x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 239 ms: 1.87x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 581 ms: 1.86x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 307 ms: 1.82x faster                                                      |
| async_tree_none            | 464 ms                                                 | 275 ms: 1.69x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 339 ms: 1.64x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 499 ms: 1.45x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 528 ms: 1.35x faster                                                      |
| regex_effbot               | 3.17 ms                                                | 2.74 ms: 1.15x faster                                                     |
| deepcopy                   | 352 us                                                 | 311 us: 1.13x faster                                                      |
| xml_etree_iterparse        | 96.7 ms                                                | 87.6 ms: 1.10x faster                                                     |
| pathlib                    | 21.5 ms                                                | 19.6 ms: 1.10x faster                                                     |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                                      |
| sqlite_synth               | 2.20 us                                                | 2.05 us: 1.07x faster                                                     |
| float                      | 80.8 ms                                                | 77.0 ms: 1.05x faster                                                     |
| deepcopy_memo              | 40.3 us                                                | 38.9 us: 1.04x faster                                                     |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                     |
| async_generators           | 384 ms                                                 | 374 ms: 1.03x faster                                                      |
| go                         | 139 ms                                                 | 141 ms: 1.01x slower                                                      |
| bpe_tokeniser              | 4.74 sec                                               | 4.79 sec: 1.01x slower                                                    |
| pycparser                  | 1.17 sec                                               | 1.19 sec: 1.02x slower                                                    |
| regex_dna                  | 168 ms                                                 | 170 ms: 1.02x slower                                                      |
| json                       | 5.02 ms                                                | 5.11 ms: 1.02x slower                                                     |
| comprehensions             | 19.8 us                                                | 20.3 us: 1.03x slower                                                     |
| spectral_norm              | 110 ms                                                 | 113 ms: 1.03x slower                                                      |
| deepcopy_reduce            | 3.08 us                                                | 3.18 us: 1.03x slower                                                     |
| pidigits                   | 184 ms                                                 | 191 ms: 1.04x slower                                                      |
| scimark_sor                | 130 ms                                                 | 136 ms: 1.05x slower                                                      |
| dulwich_log                | 78.9 ms                                                | 82.8 ms: 1.05x slower                                                     |
| docutils                   | 2.64 sec                                               | 2.80 sec: 1.06x slower                                                    |
| raytrace                   | 299 ms                                                 | 324 ms: 1.08x slower                                                      |
| logging_simple             | 6.63 us                                                | 7.17 us: 1.08x slower                                                     |
| mdp                        | 2.42 sec                                               | 2.65 sec: 1.10x slower                                                    |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.9 ms: 1.10x slower                                                     |
| regex_compile              | 142 ms                                                 | 156 ms: 1.10x slower                                                      |
| sqlalchemy_declarative     | 143 ms                                                 | 157 ms: 1.10x slower                                                      |
| deltablue                  | 3.45 ms                                                | 3.81 ms: 1.10x slower                                                     |
| tomli_loads                | 2.11 sec                                               | 2.33 sec: 1.10x slower                                                    |
| json_loads                 | 26.5 us                                                | 29.3 us: 1.10x slower                                                     |
| logging_format             | 7.35 us                                                | 8.15 us: 1.11x slower                                                     |
| html5lib                   | 63.6 ms                                                | 70.6 ms: 1.11x slower                                                     |
| chaos                      | 62.8 ms                                                | 69.8 ms: 1.11x slower                                                     |
| regex_v8                   | 20.6 ms                                                | 23.0 ms: 1.12x slower                                                     |
| thrift                     | 791 us                                                 | 886 us: 1.12x slower                                                      |
| xml_etree_generate         | 85.2 ms                                                | 95.5 ms: 1.12x slower                                                     |
| pprint_safe_repr           | 743 ms                                                 | 834 ms: 1.12x slower                                                      |
| sympy_sum                  | 166 ms                                                 | 187 ms: 1.12x slower                                                      |
| pyflate                    | 448 ms                                                 | 504 ms: 1.13x slower                                                      |
| sqlglot_normalize          | 107 ms                                                 | 121 ms: 1.13x slower                                                      |
| pprint_pformat             | 1.52 sec                                               | 1.72 sec: 1.13x slower                                                    |
| unpickle_pure_python       | 221 us                                                 | 252 us: 1.14x slower                                                      |
| crypto_pyaes               | 76.6 ms                                                | 87.7 ms: 1.14x slower                                                     |
| sqlglot_transpile          | 1.67 ms                                                | 1.92 ms: 1.15x slower                                                     |
| sympy_str                  | 292 ms                                                 | 336 ms: 1.15x slower                                                      |
| sqlglot_optimize           | 53.3 ms                                                | 61.5 ms: 1.15x slower                                                     |
| 2to3                       | 264 ms                                                 | 307 ms: 1.16x slower                                                      |
| scimark_fft                | 342 ms                                                 | 398 ms: 1.17x slower                                                      |
| sympy_integrate            | 20.5 ms                                                | 24.0 ms: 1.17x slower                                                     |
| create_gc_cycles           | 1.09 ms                                                | 1.28 ms: 1.17x slower                                                     |
| pickle_pure_python         | 308 us                                                 | 362 us: 1.18x slower                                                      |
| xml_etree_process          | 59.0 ms                                                | 69.7 ms: 1.18x slower                                                     |
| sqlglot_parse              | 1.36 ms                                                | 1.60 ms: 1.18x slower                                                     |
| sympy_expand               | 468 ms                                                 | 558 ms: 1.19x slower                                                      |
| richards                   | 45.9 ms                                                | 55.0 ms: 1.20x slower                                                     |
| genshi_xml                 | 50.2 ms                                                | 60.1 ms: 1.20x slower                                                     |
| hexiom                     | 6.17 ms                                                | 7.40 ms: 1.20x slower                                                     |
| nqueens                    | 80.1 ms                                                | 96.7 ms: 1.21x slower                                                     |
| typing_runtime_protocols   | 163 us                                                 | 199 us: 1.22x slower                                                      |
| django_template            | 34.7 ms                                                | 42.5 ms: 1.23x slower                                                     |
| scimark_monte_carlo        | 68.4 ms                                                | 83.9 ms: 1.23x slower                                                     |
| json_dumps                 | 10.4 ms                                                | 12.7 ms: 1.23x slower                                                     |
| scimark_lu                 | 114 ms                                                 | 140 ms: 1.23x slower                                                      |
| richards_super             | 51.9 ms                                                | 63.9 ms: 1.23x slower                                                     |
| genshi_text                | 22.8 ms                                                | 28.2 ms: 1.24x slower                                                     |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.25x slower                                                      |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.81 ms: 1.32x slower                                                     |
| fannkuch                   | 372 ms                                                 | 497 ms: 1.33x slower                                                      |
| telco                      | 6.53 ms                                                | 8.78 ms: 1.35x slower                                                     |
| python_startup_no_site     | 7.16 ms                                                | 9.68 ms: 1.35x slower                                                     |
| coverage                   | 71.4 ms                                                | 97.7 ms: 1.37x slower                                                     |
| mako                       | 11.0 ms                                                | 16.0 ms: 1.45x slower                                                     |
| nbody                      | 89.3 ms                                                | 131 ms: 1.46x slower                                                      |
| python_startup             | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                     |
| bench_thread_pool          | 941 us                                                 | 3.32 ms: 3.53x slower                                                     |
| bench_mp_pool              | 10.8 ms                                                | 95.6 ms: 8.85x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.08x slower                                                              |

Benchmark hidden because not significant (4): pylint, asyncio_websockets, generators, logging_silent
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250303-3.14.0a5+-e2f1387-NOGIL/bm-20250303-vultr-x86_64-faster%2dcpython-use_stackrefs-3.14.0a5+-e2f1387.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.043x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.36x