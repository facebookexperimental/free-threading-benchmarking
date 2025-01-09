# Results vs. 3.12.6

- fork: Yhg1s
- ref: list_realloc
- machine: linux-x86_64
- commit hash: 7263d1e
- commit date: 2025-01-09
- overall geometric mean: 1.179x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250109-linux-x86_64-Yhg1s-list_realloc-3.14.0a3+-7263d1e |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 653 ms: 1.43x slower                                          |
| docutils       | 4.00 sec                                               | 4.77 sec: 1.19x slower                                        |
| html5lib       | 88.9 ms                                                | 121 ms: 1.36x slower                                          |
| Geometric mean | (ref)                                                  | 1.33x slower                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250109-linux-x86_64-Yhg1s-list_realloc-3.14.0a3+-7263d1e |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 984 ms: 1.97x faster                                          |
| async_tree_io              | 1.85 sec                                               | 1.05 sec: 1.76x faster                                        |
| async_tree_memoization     | 977 ms                                                 | 598 ms: 1.63x faster                                          |
| async_tree_none_tg         | 704 ms                                                 | 439 ms: 1.61x faster                                          |
| async_tree_memoization_tg  | 930 ms                                                 | 601 ms: 1.55x faster                                          |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 752 ms: 1.46x faster                                          |
| async_tree_none            | 741 ms                                                 | 512 ms: 1.45x faster                                          |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 844 ms: 1.28x faster                                          |
| asyncio_websockets         | 748 ms                                                 | 779 ms: 1.04x slower                                          |
| async_generators           | 589 ms                                                 | 674 ms: 1.14x slower                                          |
| coroutines                 | 29.5 ms                                                | 36.1 ms: 1.22x slower                                         |
| Geometric mean             | (ref)                                                  | 1.35x faster                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250109-linux-x86_64-Yhg1s-list_realloc-3.14.0a3+-7263d1e |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| pidigits       | 250 ms                                                 | 261 ms: 1.05x slower                                          |
| float          | 123 ms                                                 | 143 ms: 1.17x slower                                          |
| nbody          | 119 ms                                                 | 179 ms: 1.50x slower                                          |
| Geometric mean | (ref)                                                  | 1.22x slower                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250109-linux-x86_64-Yhg1s-list_realloc-3.14.0a3+-7263d1e |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.34 ms: 1.18x faster                                         |
| regex_dna      | 278 ms                                                 | 327 ms: 1.17x slower                                          |
| regex_compile  | 187 ms                                                 | 228 ms: 1.22x slower                                          |
| regex_v8       | 32.5 ms                                                | 41.0 ms: 1.26x slower                                         |
| Geometric mean | (ref)                                                  | 1.11x slower                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250109-linux-x86_64-Yhg1s-list_realloc-3.14.0a3+-7263d1e |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| xml_etree_parse      | 241 ms                                                 | 222 ms: 1.09x faster                                          |
| json_loads           | 37.9 us                                                | 40.0 us: 1.05x slower                                         |
| xml_etree_generate   | 127 ms                                                 | 142 ms: 1.12x slower                                          |
| tomli_loads          | 2.88 sec                                               | 3.25 sec: 1.13x slower                                        |
| json_dumps           | 14.3 ms                                                | 16.7 ms: 1.17x slower                                         |
| xml_etree_process    | 83.7 ms                                                | 101 ms: 1.21x slower                                          |
| unpickle_pure_python | 300 us                                                 | 410 us: 1.37x slower                                          |
| pickle_pure_python   | 436 us                                                 | 661 us: 1.52x slower                                          |
| Geometric mean       | (ref)                                                  | 1.15x slower                                                  |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250109-linux-x86_64-Yhg1s-list_realloc-3.14.0a3+-7263d1e |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 23.8 ms: 1.35x slower                                         |
| python_startup         | 23.7 ms                                                | 38.1 ms: 1.61x slower                                         |
| Geometric mean         | (ref)                                                  | 1.48x slower                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250109-linux-x86_64-Yhg1s-list_realloc-3.14.0a3+-7263d1e |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| genshi_text     | 30.2 ms                                                | 39.5 ms: 1.31x slower                                         |
| genshi_xml      | 67.6 ms                                                | 89.0 ms: 1.32x slower                                         |
| django_template | 44.9 ms                                                | 67.0 ms: 1.49x slower                                         |
| mako            | 15.7 ms                                                | 30.4 ms: 1.93x slower                                         |
| Geometric mean  | (ref)                                                  | 1.49x slower                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250109-linux-x86_64-Yhg1s-list_realloc-3.14.0a3+-7263d1e |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 984 ms: 1.97x faster                                          |
| async_tree_io              | 1.85 sec                                               | 1.05 sec: 1.76x faster                                        |
| async_tree_memoization     | 977 ms                                                 | 598 ms: 1.63x faster                                          |
| async_tree_none_tg         | 704 ms                                                 | 439 ms: 1.61x faster                                          |
| async_tree_memoization_tg  | 930 ms                                                 | 601 ms: 1.55x faster                                          |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 752 ms: 1.46x faster                                          |
| async_tree_none            | 741 ms                                                 | 512 ms: 1.45x faster                                          |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 844 ms: 1.28x faster                                          |
| regex_effbot               | 5.13 ms                                                | 4.34 ms: 1.18x faster                                         |
| xml_etree_parse            | 241 ms                                                 | 222 ms: 1.09x faster                                          |
| asyncio_websockets         | 748 ms                                                 | 779 ms: 1.04x slower                                          |
| pidigits                   | 250 ms                                                 | 261 ms: 1.05x slower                                          |
| json_loads                 | 37.9 us                                                | 40.0 us: 1.05x slower                                         |
| spectral_norm              | 156 ms                                                 | 167 ms: 1.07x slower                                          |
| deepcopy_memo              | 52.4 us                                                | 56.3 us: 1.07x slower                                         |
| json                       | 6.85 ms                                                | 7.37 ms: 1.08x slower                                         |
| pathlib                    | 31.6 ms                                                | 34.4 ms: 1.09x slower                                         |
| xml_etree_generate         | 127 ms                                                 | 142 ms: 1.12x slower                                          |
| sqlglot_optimize           | 76.0 ms                                                | 85.3 ms: 1.12x slower                                         |
| tomli_loads                | 2.88 sec                                               | 3.25 sec: 1.13x slower                                        |
| sympy_str                  | 385 ms                                                 | 436 ms: 1.13x slower                                          |
| async_generators           | 589 ms                                                 | 674 ms: 1.14x slower                                          |
| sqlglot_normalize          | 157 ms                                                 | 182 ms: 1.16x slower                                          |
| float                      | 123 ms                                                 | 143 ms: 1.17x slower                                          |
| scimark_fft                | 500 ms                                                 | 583 ms: 1.17x slower                                          |
| json_dumps                 | 14.3 ms                                                | 16.7 ms: 1.17x slower                                         |
| regex_dna                  | 278 ms                                                 | 327 ms: 1.17x slower                                          |
| deepcopy_reduce            | 4.04 us                                                | 4.79 us: 1.19x slower                                         |
| crypto_pyaes               | 107 ms                                                 | 128 ms: 1.19x slower                                          |
| dulwich_log                | 100 ms                                                 | 119 ms: 1.19x slower                                          |
| docutils                   | 4.00 sec                                               | 4.77 sec: 1.19x slower                                        |
| xml_etree_process          | 83.7 ms                                                | 101 ms: 1.21x slower                                          |
| coroutines                 | 29.5 ms                                                | 36.1 ms: 1.22x slower                                         |
| regex_compile              | 187 ms                                                 | 228 ms: 1.22x slower                                          |
| pylint                     | 465 ms                                                 | 570 ms: 1.23x slower                                          |
| nqueens                    | 117 ms                                                 | 145 ms: 1.24x slower                                          |
| regex_v8                   | 32.5 ms                                                | 41.0 ms: 1.26x slower                                         |
| sympy_expand               | 582 ms                                                 | 736 ms: 1.26x slower                                          |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 8.50 ms: 1.27x slower                                         |
| mdp                        | 3.97 sec                                               | 5.15 sec: 1.30x slower                                        |
| genshi_text                | 30.2 ms                                                | 39.5 ms: 1.31x slower                                         |
| sympy_sum                  | 222 ms                                                 | 290 ms: 1.31x slower                                          |
| bpe_tokeniser              | 6.59 sec                                               | 8.65 sec: 1.31x slower                                        |
| genshi_xml                 | 67.6 ms                                                | 89.0 ms: 1.32x slower                                         |
| meteor_contest             | 146 ms                                                 | 193 ms: 1.32x slower                                          |
| pyflate                    | 727 ms                                                 | 962 ms: 1.32x slower                                          |
| sqlalchemy_declarative     | 218 ms                                                 | 290 ms: 1.33x slower                                          |
| scimark_monte_carlo        | 96.4 ms                                                | 129 ms: 1.33x slower                                          |
| typing_runtime_protocols   | 224 us                                                 | 301 us: 1.34x slower                                          |
| pprint_safe_repr           | 967 ms                                                 | 1.30 sec: 1.34x slower                                        |
| scimark_lu                 | 152 ms                                                 | 205 ms: 1.35x slower                                          |
| python_startup_no_site     | 17.6 ms                                                | 23.8 ms: 1.35x slower                                         |
| html5lib                   | 88.9 ms                                                | 121 ms: 1.36x slower                                          |
| coverage                   | 95.4 ms                                                | 130 ms: 1.37x slower                                          |
| unpickle_pure_python       | 300 us                                                 | 410 us: 1.37x slower                                          |
| comprehensions             | 27.1 us                                                | 37.2 us: 1.37x slower                                         |
| generators                 | 41.1 ms                                                | 56.9 ms: 1.38x slower                                         |
| richards                   | 60.3 ms                                                | 84.0 ms: 1.39x slower                                         |
| pprint_pformat             | 1.98 sec                                               | 2.80 sec: 1.41x slower                                        |
| richards_super             | 72.8 ms                                                | 103 ms: 1.42x slower                                          |
| 2to3                       | 456 ms                                                 | 653 ms: 1.43x slower                                          |
| logging_simple             | 9.45 us                                                | 13.7 us: 1.45x slower                                         |
| telco                      | 9.59 ms                                                | 14.1 ms: 1.47x slower                                         |
| django_template            | 44.9 ms                                                | 67.0 ms: 1.49x slower                                         |
| thrift                     | 1.06 ms                                                | 1.59 ms: 1.50x slower                                         |
| scimark_sor                | 167 ms                                                 | 250 ms: 1.50x slower                                          |
| sympy_integrate            | 29.8 ms                                                | 44.7 ms: 1.50x slower                                         |
| nbody                      | 119 ms                                                 | 179 ms: 1.50x slower                                          |
| pickle_pure_python         | 436 us                                                 | 661 us: 1.52x slower                                          |
| fannkuch                   | 540 ms                                                 | 826 ms: 1.53x slower                                          |
| hexiom                     | 8.27 ms                                                | 12.7 ms: 1.54x slower                                         |
| bench_thread_pool          | 3.48 ms                                                | 5.37 ms: 1.54x slower                                         |
| gc_traversal               | 5.86 ms                                                | 9.15 ms: 1.56x slower                                         |
| raytrace                   | 408 ms                                                 | 641 ms: 1.57x slower                                          |
| chaos                      | 84.9 ms                                                | 135 ms: 1.59x slower                                          |
| python_startup             | 23.7 ms                                                | 38.1 ms: 1.61x slower                                         |
| logging_format             | 9.59 us                                                | 15.4 us: 1.61x slower                                         |
| go                         | 172 ms                                                 | 287 ms: 1.66x slower                                          |
| sqlalchemy_imperative      | 24.7 ms                                                | 41.3 ms: 1.67x slower                                         |
| sqlglot_transpile          | 2.34 ms                                                | 3.97 ms: 1.70x slower                                         |
| logging_silent             | 139 ns                                                 | 244 ns: 1.75x slower                                          |
| sqlglot_parse              | 1.79 ms                                                | 3.25 ms: 1.82x slower                                         |
| mako                       | 15.7 ms                                                | 30.4 ms: 1.93x slower                                         |
| deltablue                  | 4.27 ms                                                | 9.95 ms: 2.33x slower                                         |
| create_gc_cycles           | 1.94 ms                                                | 6.43 ms: 3.32x slower                                         |
| bench_mp_pool              | 20.7 ms                                                | 111 ms: 5.36x slower                                          |
| Geometric mean             | (ref)                                                  | 1.26x slower                                                  |

Benchmark hidden because not significant (4): pycparser, deepcopy, xml_etree_iterparse, sqlite_synth
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250109-3.14.0a3+-7263d1e-NOGIL/bm-20250109-linux-x86_64-Yhg1s-list_realloc-3.14.0a3+-7263d1e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.179x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.18x
- 95% likely to have a slowdown of 1.17x
- 99% likely to have a slowdown of 1.15x

# Memory
- memory change: 1.34x