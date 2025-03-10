# Results vs. 3.12.6

- fork: python
- ref: 98fa4a49fecbac3c990a
- machine: linux-x86_64
- commit hash: 98fa4a4
- commit date: 2025-03-09
- overall geometric mean: 1.023x slower
- HPT reliability: 99.94%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 553 ms: 1.21x slower                                                   |
| docutils       | 4.00 sec                                               | 4.18 sec: 1.05x slower                                                 |
| html5lib       | 88.9 ms                                                | 98.4 ms: 1.11x slower                                                  |
| Geometric mean | (ref)                                                  | 1.12x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 772 ms: 2.51x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 826 ms: 2.24x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 356 ms: 1.98x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 474 ms: 1.96x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 509 ms: 1.92x faster                                                   |
| async_tree_none            | 741 ms                                                 | 396 ms: 1.87x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 644 ms: 1.71x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 712 ms: 1.51x faster                                                   |
| coroutines                 | 29.5 ms                                                | 30.8 ms: 1.04x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.61x faster                                                           |

Benchmark hidden because not significant (2): async_generators, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 103 ms: 1.20x faster                                                   |
| nbody          | 119 ms                                                 | 181 ms: 1.52x slower                                                   |
| Geometric mean | (ref)                                                  | 1.09x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.53 ms: 1.13x faster                                                  |
| regex_compile  | 187 ms                                                 | 198 ms: 1.06x slower                                                   |
| regex_dna      | 278 ms                                                 | 296 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 169 ms                                                 | 132 ms: 1.28x faster                                                   |
| xml_etree_parse      | 241 ms                                                 | 205 ms: 1.17x faster                                                   |
| tomli_loads          | 2.88 sec                                               | 3.05 sec: 1.06x slower                                                 |
| unpickle_pure_python | 300 us                                                 | 338 us: 1.13x slower                                                   |
| json_loads           | 37.9 us                                                | 42.8 us: 1.13x slower                                                  |
| pickle_pure_python   | 436 us                                                 | 500 us: 1.15x slower                                                   |
| xml_etree_process    | 83.7 ms                                                | 96.3 ms: 1.15x slower                                                  |
| json_dumps           | 14.3 ms                                                | 19.4 ms: 1.36x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.06x slower                                                           |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 23.9 ms: 1.36x slower                                                  |
| python_startup         | 23.7 ms                                                | 35.5 ms: 1.50x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.42x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 44.9 ms                                                | 54.7 ms: 1.22x slower                                                  |
| genshi_xml      | 67.6 ms                                                | 86.9 ms: 1.29x slower                                                  |
| genshi_text     | 30.2 ms                                                | 39.5 ms: 1.31x slower                                                  |
| mako            | 15.7 ms                                                | 23.6 ms: 1.50x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.32x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 772 ms: 2.51x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 826 ms: 2.24x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 356 ms: 1.98x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 474 ms: 1.96x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 509 ms: 1.92x faster                                                   |
| async_tree_none            | 741 ms                                                 | 396 ms: 1.87x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 644 ms: 1.71x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 712 ms: 1.51x faster                                                   |
| gc_traversal               | 5.86 ms                                                | 4.03 ms: 1.46x faster                                                  |
| xml_etree_iterparse        | 169 ms                                                 | 132 ms: 1.28x faster                                                   |
| float                      | 123 ms                                                 | 103 ms: 1.20x faster                                                   |
| xml_etree_parse            | 241 ms                                                 | 205 ms: 1.17x faster                                                   |
| pycparser                  | 1.79 sec                                               | 1.56 sec: 1.15x faster                                                 |
| regex_effbot               | 5.13 ms                                                | 4.53 ms: 1.13x faster                                                  |
| sqlite_synth               | 3.87 us                                                | 3.43 us: 1.13x faster                                                  |
| deepcopy                   | 468 us                                                 | 430 us: 1.09x faster                                                   |
| sqlglot_normalize          | 157 ms                                                 | 148 ms: 1.06x faster                                                   |
| deepcopy_memo              | 52.4 us                                                | 49.9 us: 1.05x faster                                                  |
| go                         | 172 ms                                                 | 178 ms: 1.03x slower                                                   |
| comprehensions             | 27.1 us                                                | 28.2 us: 1.04x slower                                                  |
| coroutines                 | 29.5 ms                                                | 30.8 ms: 1.04x slower                                                  |
| docutils                   | 4.00 sec                                               | 4.18 sec: 1.05x slower                                                 |
| tomli_loads                | 2.88 sec                                               | 3.05 sec: 1.06x slower                                                 |
| deepcopy_reduce            | 4.04 us                                                | 4.28 us: 1.06x slower                                                  |
| regex_compile              | 187 ms                                                 | 198 ms: 1.06x slower                                                   |
| regex_dna                  | 278 ms                                                 | 296 ms: 1.06x slower                                                   |
| logging_silent             | 139 ns                                                 | 148 ns: 1.07x slower                                                   |
| pyflate                    | 727 ms                                                 | 780 ms: 1.07x slower                                                   |
| mdp                        | 3.97 sec                                               | 4.30 sec: 1.08x slower                                                 |
| logging_format             | 9.59 us                                                | 10.4 us: 1.09x slower                                                  |
| sqlglot_optimize           | 76.0 ms                                                | 83.0 ms: 1.09x slower                                                  |
| raytrace                   | 408 ms                                                 | 446 ms: 1.09x slower                                                   |
| crypto_pyaes               | 107 ms                                                 | 118 ms: 1.10x slower                                                   |
| html5lib                   | 88.9 ms                                                | 98.4 ms: 1.11x slower                                                  |
| generators                 | 41.1 ms                                                | 45.6 ms: 1.11x slower                                                  |
| sympy_sum                  | 222 ms                                                 | 247 ms: 1.11x slower                                                   |
| scimark_fft                | 500 ms                                                 | 565 ms: 1.13x slower                                                   |
| unpickle_pure_python       | 300 us                                                 | 338 us: 1.13x slower                                                   |
| sympy_str                  | 385 ms                                                 | 435 ms: 1.13x slower                                                   |
| json_loads                 | 37.9 us                                                | 42.8 us: 1.13x slower                                                  |
| thrift                     | 1.06 ms                                                | 1.20 ms: 1.14x slower                                                  |
| chaos                      | 84.9 ms                                                | 96.8 ms: 1.14x slower                                                  |
| sympy_integrate            | 29.8 ms                                                | 34.0 ms: 1.14x slower                                                  |
| sqlglot_transpile          | 2.34 ms                                                | 2.68 ms: 1.15x slower                                                  |
| bpe_tokeniser              | 6.59 sec                                               | 7.55 sec: 1.15x slower                                                 |
| pickle_pure_python         | 436 us                                                 | 500 us: 1.15x slower                                                   |
| xml_etree_process          | 83.7 ms                                                | 96.3 ms: 1.15x slower                                                  |
| pprint_pformat             | 1.98 sec                                               | 2.28 sec: 1.15x slower                                                 |
| richards                   | 60.3 ms                                                | 70.4 ms: 1.17x slower                                                  |
| pprint_safe_repr           | 967 ms                                                 | 1.13 sec: 1.17x slower                                                 |
| scimark_lu                 | 152 ms                                                 | 180 ms: 1.18x slower                                                   |
| typing_runtime_protocols   | 224 us                                                 | 267 us: 1.19x slower                                                   |
| hexiom                     | 8.27 ms                                                | 9.93 ms: 1.20x slower                                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 116 ms: 1.20x slower                                                   |
| 2to3                       | 456 ms                                                 | 553 ms: 1.21x slower                                                   |
| sqlalchemy_imperative      | 24.7 ms                                                | 29.9 ms: 1.21x slower                                                  |
| nqueens                    | 117 ms                                                 | 142 ms: 1.22x slower                                                   |
| django_template            | 44.9 ms                                                | 54.7 ms: 1.22x slower                                                  |
| sqlglot_parse              | 1.79 ms                                                | 2.18 ms: 1.22x slower                                                  |
| sympy_expand               | 582 ms                                                 | 717 ms: 1.23x slower                                                   |
| fannkuch                   | 540 ms                                                 | 669 ms: 1.24x slower                                                   |
| deltablue                  | 4.27 ms                                                | 5.31 ms: 1.25x slower                                                  |
| meteor_contest             | 146 ms                                                 | 185 ms: 1.26x slower                                                   |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 8.54 ms: 1.27x slower                                                  |
| richards_super             | 72.8 ms                                                | 92.8 ms: 1.28x slower                                                  |
| bench_thread_pool          | 3.48 ms                                                | 4.46 ms: 1.28x slower                                                  |
| genshi_xml                 | 67.6 ms                                                | 86.9 ms: 1.29x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 2.52 ms: 1.30x slower                                                  |
| genshi_text                | 30.2 ms                                                | 39.5 ms: 1.31x slower                                                  |
| telco                      | 9.59 ms                                                | 12.7 ms: 1.32x slower                                                  |
| json_dumps                 | 14.3 ms                                                | 19.4 ms: 1.36x slower                                                  |
| python_startup_no_site     | 17.6 ms                                                | 23.9 ms: 1.36x slower                                                  |
| python_startup             | 23.7 ms                                                | 35.5 ms: 1.50x slower                                                  |
| mako                       | 15.7 ms                                                | 23.6 ms: 1.50x slower                                                  |
| nbody                      | 119 ms                                                 | 181 ms: 1.52x slower                                                   |
| coverage                   | 95.4 ms                                                | 147 ms: 1.54x slower                                                   |
| bench_mp_pool              | 20.7 ms                                                | 87.1 ms: 4.21x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.05x slower                                                           |

Benchmark hidden because not significant (13): spectral_norm, pathlib, async_generators, pylint, dulwich_log, logging_simple, scimark_sor, regex_v8, sqlalchemy_declarative, pidigits, asyncio_websockets, json, xml_etree_generate
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250309-3.14.0a5+-98fa4a4-NOGIL/bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.023x slower

# HPT report

- Reliability score: 99.94% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.36x