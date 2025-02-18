# Results vs. 3.12.6

- fork: python
- ref: 99d965635ae2ac4bffdc
- machine: linux-x86_64
- commit hash: 99d9656
- commit date: 2025-02-17
- overall geometric mean: 1.014x slower
- HPT reliability: 99.81%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 539 ms: 1.18x slower                                                   |
| html5lib       | 88.9 ms                                                | 95.3 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                  | 1.09x slower                                                           |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 814 ms: 2.38x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 871 ms: 2.12x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 349 ms: 2.02x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 496 ms: 1.87x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 547 ms: 1.79x faster                                                   |
| async_tree_none            | 741 ms                                                 | 417 ms: 1.78x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 668 ms: 1.65x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 737 ms: 1.46x faster                                                   |
| async_generators           | 589 ms                                                 | 564 ms: 1.04x faster                                                   |
| coroutines                 | 29.5 ms                                                | 31.5 ms: 1.07x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.57x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 104 ms: 1.18x faster                                                   |
| nbody          | 119 ms                                                 | 180 ms: 1.51x slower                                                   |
| Geometric mean | (ref)                                                  | 1.08x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.66 ms: 1.10x faster                                                  |
| regex_compile  | 187 ms                                                 | 199 ms: 1.07x slower                                                   |
| regex_dna      | 278 ms                                                 | 299 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x slower                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 169 ms                                                 | 139 ms: 1.22x faster                                                   |
| xml_etree_parse      | 241 ms                                                 | 210 ms: 1.15x faster                                                   |
| tomli_loads          | 2.88 sec                                               | 3.05 sec: 1.06x slower                                                 |
| json_loads           | 37.9 us                                                | 41.8 us: 1.10x slower                                                  |
| pickle_pure_python   | 436 us                                                 | 483 us: 1.11x slower                                                   |
| xml_etree_process    | 83.7 ms                                                | 95.8 ms: 1.14x slower                                                  |
| json_dumps           | 14.3 ms                                                | 16.5 ms: 1.15x slower                                                  |
| unpickle_pure_python | 300 us                                                 | 346 us: 1.15x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.04x slower                                                           |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 20.7 ms: 1.18x slower                                                  |
| python_startup         | 23.7 ms                                                | 31.7 ms: 1.34x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.25x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 79.3 ms: 1.17x slower                                                  |
| django_template | 44.9 ms                                                | 53.0 ms: 1.18x slower                                                  |
| genshi_text     | 30.2 ms                                                | 39.4 ms: 1.31x slower                                                  |
| mako            | 15.7 ms                                                | 22.2 ms: 1.41x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.26x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 814 ms: 2.38x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 871 ms: 2.12x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 349 ms: 2.02x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 496 ms: 1.87x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 547 ms: 1.79x faster                                                   |
| gc_traversal               | 5.86 ms                                                | 3.28 ms: 1.78x faster                                                  |
| async_tree_none            | 741 ms                                                 | 417 ms: 1.78x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 668 ms: 1.65x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 737 ms: 1.46x faster                                                   |
| xml_etree_iterparse        | 169 ms                                                 | 139 ms: 1.22x faster                                                   |
| float                      | 123 ms                                                 | 104 ms: 1.18x faster                                                   |
| xml_etree_parse            | 241 ms                                                 | 210 ms: 1.15x faster                                                   |
| deepcopy                   | 468 us                                                 | 417 us: 1.12x faster                                                   |
| spectral_norm              | 156 ms                                                 | 139 ms: 1.12x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.66 ms: 1.10x faster                                                  |
| pycparser                  | 1.79 sec                                               | 1.66 sec: 1.08x faster                                                 |
| sqlite_synth               | 3.87 us                                                | 3.64 us: 1.07x faster                                                  |
| comprehensions             | 27.1 us                                                | 25.7 us: 1.05x faster                                                  |
| sqlalchemy_declarative     | 218 ms                                                 | 207 ms: 1.05x faster                                                   |
| async_generators           | 589 ms                                                 | 564 ms: 1.04x faster                                                   |
| mdp                        | 3.97 sec                                               | 4.07 sec: 1.03x slower                                                 |
| deepcopy_reduce            | 4.04 us                                                | 4.16 us: 1.03x slower                                                  |
| bpe_tokeniser              | 6.59 sec                                               | 6.92 sec: 1.05x slower                                                 |
| tomli_loads                | 2.88 sec                                               | 3.05 sec: 1.06x slower                                                 |
| scimark_fft                | 500 ms                                                 | 531 ms: 1.06x slower                                                   |
| coroutines                 | 29.5 ms                                                | 31.5 ms: 1.07x slower                                                  |
| regex_compile              | 187 ms                                                 | 199 ms: 1.07x slower                                                   |
| html5lib                   | 88.9 ms                                                | 95.3 ms: 1.07x slower                                                  |
| sqlglot_optimize           | 76.0 ms                                                | 81.4 ms: 1.07x slower                                                  |
| regex_dna                  | 278 ms                                                 | 299 ms: 1.07x slower                                                   |
| raytrace                   | 408 ms                                                 | 441 ms: 1.08x slower                                                   |
| sympy_str                  | 385 ms                                                 | 419 ms: 1.09x slower                                                   |
| sympy_sum                  | 222 ms                                                 | 243 ms: 1.10x slower                                                   |
| richards_super             | 72.8 ms                                                | 80.2 ms: 1.10x slower                                                  |
| generators                 | 41.1 ms                                                | 45.3 ms: 1.10x slower                                                  |
| json_loads                 | 37.9 us                                                | 41.8 us: 1.10x slower                                                  |
| pickle_pure_python         | 436 us                                                 | 483 us: 1.11x slower                                                   |
| chaos                      | 84.9 ms                                                | 94.2 ms: 1.11x slower                                                  |
| crypto_pyaes               | 107 ms                                                 | 119 ms: 1.11x slower                                                   |
| nqueens                    | 117 ms                                                 | 131 ms: 1.12x slower                                                   |
| sympy_integrate            | 29.8 ms                                                | 33.4 ms: 1.12x slower                                                  |
| bench_thread_pool          | 3.48 ms                                                | 3.94 ms: 1.13x slower                                                  |
| xml_etree_process          | 83.7 ms                                                | 95.8 ms: 1.14x slower                                                  |
| richards                   | 60.3 ms                                                | 69.4 ms: 1.15x slower                                                  |
| json_dumps                 | 14.3 ms                                                | 16.5 ms: 1.15x slower                                                  |
| pprint_safe_repr           | 967 ms                                                 | 1.11 sec: 1.15x slower                                                 |
| unpickle_pure_python       | 300 us                                                 | 346 us: 1.15x slower                                                   |
| go                         | 172 ms                                                 | 200 ms: 1.16x slower                                                   |
| scimark_monte_carlo        | 96.4 ms                                                | 112 ms: 1.16x slower                                                   |
| pprint_pformat             | 1.98 sec                                               | 2.30 sec: 1.16x slower                                                 |
| json                       | 6.85 ms                                                | 7.97 ms: 1.16x slower                                                  |
| sqlglot_transpile          | 2.34 ms                                                | 2.74 ms: 1.17x slower                                                  |
| genshi_xml                 | 67.6 ms                                                | 79.3 ms: 1.17x slower                                                  |
| scimark_lu                 | 152 ms                                                 | 179 ms: 1.17x slower                                                   |
| logging_format             | 9.59 us                                                | 11.3 us: 1.18x slower                                                  |
| python_startup_no_site     | 17.6 ms                                                | 20.7 ms: 1.18x slower                                                  |
| django_template            | 44.9 ms                                                | 53.0 ms: 1.18x slower                                                  |
| 2to3                       | 456 ms                                                 | 539 ms: 1.18x slower                                                   |
| typing_runtime_protocols   | 224 us                                                 | 268 us: 1.19x slower                                                   |
| thrift                     | 1.06 ms                                                | 1.27 ms: 1.20x slower                                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 8.06 ms: 1.20x slower                                                  |
| meteor_contest             | 146 ms                                                 | 178 ms: 1.21x slower                                                   |
| telco                      | 9.59 ms                                                | 11.7 ms: 1.22x slower                                                  |
| hexiom                     | 8.27 ms                                                | 10.2 ms: 1.23x slower                                                  |
| deltablue                  | 4.27 ms                                                | 5.27 ms: 1.23x slower                                                  |
| sympy_expand               | 582 ms                                                 | 722 ms: 1.24x slower                                                   |
| fannkuch                   | 540 ms                                                 | 673 ms: 1.24x slower                                                   |
| sqlalchemy_imperative      | 24.7 ms                                                | 31.0 ms: 1.26x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 2.44 ms: 1.26x slower                                                  |
| sqlglot_parse              | 1.79 ms                                                | 2.25 ms: 1.26x slower                                                  |
| genshi_text                | 30.2 ms                                                | 39.4 ms: 1.31x slower                                                  |
| python_startup             | 23.7 ms                                                | 31.7 ms: 1.34x slower                                                  |
| mako                       | 15.7 ms                                                | 22.2 ms: 1.41x slower                                                  |
| coverage                   | 95.4 ms                                                | 140 ms: 1.47x slower                                                   |
| nbody                      | 119 ms                                                 | 180 ms: 1.51x slower                                                   |
| bench_mp_pool              | 20.7 ms                                                | 84.3 ms: 4.07x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.04x slower                                                           |

Benchmark hidden because not significant (14): deepcopy_memo, pidigits, pylint, pathlib, logging_simple, sqlglot_normalize, scimark_sor, xml_etree_generate, dulwich_log, docutils, logging_silent, pyflate, regex_v8, asyncio_websockets
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250217-3.14.0a5+-99d9656-NOGIL/bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.014x slower

# HPT report

- Reliability score: 99.81% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.35x