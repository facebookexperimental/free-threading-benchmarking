# Results vs. 3.12.6

- fork: python
- ref: bc26f95e8ff60ccca981
- machine: linux-x86_64
- commit hash: bc26f95
- commit date: 2025-03-22
- overall geometric mean: 1.004x faster
- HPT reliability: 88.03%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.38x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 506 ms: 1.11x slower                                                   |
| html5lib       | 88.9 ms                                                | 94.8 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x slower                                                           |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 730 ms: 2.65x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 803 ms: 2.30x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 331 ms: 2.12x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 441 ms: 2.11x faster                                                   |
| async_tree_none            | 741 ms                                                 | 384 ms: 1.93x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 509 ms: 1.92x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 633 ms: 1.74x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 679 ms: 1.59x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 712 ms: 1.05x faster                                                   |
| async_generators           | 589 ms                                                 | 574 ms: 1.03x faster                                                   |
| asyncio_tcp                | 923 ms                                                 | 1.02 sec: 1.11x slower                                                 |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.21 sec: 1.14x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.52x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 101 ms: 1.21x faster                                                   |
| pidigits       | 250 ms                                                 | 226 ms: 1.10x faster                                                   |
| nbody          | 119 ms                                                 | 167 ms: 1.40x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.37 ms: 1.17x faster                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (3): regex_compile, regex_dna, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 169 ms                                                 | 137 ms: 1.23x faster                                                   |
| pickle_dict          | 52.7 us                                                | 43.2 us: 1.22x faster                                                  |
| xml_etree_parse      | 241 ms                                                 | 207 ms: 1.16x faster                                                   |
| xml_etree_generate   | 127 ms                                                 | 136 ms: 1.07x slower                                                   |
| tomli_loads          | 2.88 sec                                               | 3.11 sec: 1.08x slower                                                 |
| unpickle             | 21.2 us                                                | 23.9 us: 1.12x slower                                                  |
| json_loads           | 37.9 us                                                | 43.6 us: 1.15x slower                                                  |
| json_dumps           | 14.3 ms                                                | 16.5 ms: 1.15x slower                                                  |
| xml_etree_process    | 83.7 ms                                                | 96.9 ms: 1.16x slower                                                  |
| pickle_pure_python   | 436 us                                                 | 506 us: 1.16x slower                                                   |
| unpickle_list        | 6.83 us                                                | 8.15 us: 1.19x slower                                                  |
| unpickle_pure_python | 300 us                                                 | 358 us: 1.20x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.04x slower                                                           |

Benchmark hidden because not significant (2): pickle_list, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 21.4 ms: 1.21x slower                                                  |
| python_startup         | 23.7 ms                                                | 29.4 ms: 1.24x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.23x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 76.8 ms: 1.14x slower                                                  |
| django_template | 44.9 ms                                                | 52.4 ms: 1.17x slower                                                  |
| genshi_text     | 30.2 ms                                                | 36.8 ms: 1.22x slower                                                  |
| mako            | 15.7 ms                                                | 23.1 ms: 1.47x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.24x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 730 ms: 2.65x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 803 ms: 2.30x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 331 ms: 2.12x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 441 ms: 2.11x faster                                                   |
| async_tree_none            | 741 ms                                                 | 384 ms: 1.93x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 509 ms: 1.92x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 633 ms: 1.74x faster                                                   |
| gc_traversal               | 5.86 ms                                                | 3.51 ms: 1.67x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 679 ms: 1.59x faster                                                   |
| xml_etree_iterparse        | 169 ms                                                 | 137 ms: 1.23x faster                                                   |
| pickle_dict                | 52.7 us                                                | 43.2 us: 1.22x faster                                                  |
| float                      | 123 ms                                                 | 101 ms: 1.21x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.37 ms: 1.17x faster                                                  |
| deepcopy                   | 468 us                                                 | 403 us: 1.16x faster                                                   |
| xml_etree_parse            | 241 ms                                                 | 207 ms: 1.16x faster                                                   |
| pycparser                  | 1.79 sec                                               | 1.59 sec: 1.13x faster                                                 |
| pidigits                   | 250 ms                                                 | 226 ms: 1.10x faster                                                   |
| pathlib                    | 31.6 ms                                                | 28.9 ms: 1.09x faster                                                  |
| pylint                     | 465 ms                                                 | 428 ms: 1.09x faster                                                   |
| spectral_norm              | 156 ms                                                 | 147 ms: 1.06x faster                                                   |
| deepcopy_memo              | 52.4 us                                                | 49.8 us: 1.05x faster                                                  |
| asyncio_websockets         | 748 ms                                                 | 712 ms: 1.05x faster                                                   |
| comprehensions             | 27.1 us                                                | 26.1 us: 1.04x faster                                                  |
| logging_simple             | 9.45 us                                                | 9.08 us: 1.04x faster                                                  |
| pyflate                    | 727 ms                                                 | 704 ms: 1.03x faster                                                   |
| async_generators           | 589 ms                                                 | 574 ms: 1.03x faster                                                   |
| crypto_pyaes               | 107 ms                                                 | 110 ms: 1.03x slower                                                   |
| chaos                      | 84.9 ms                                                | 88.0 ms: 1.04x slower                                                  |
| raytrace                   | 408 ms                                                 | 428 ms: 1.05x slower                                                   |
| bpe_tokeniser              | 6.59 sec                                               | 6.95 sec: 1.05x slower                                                 |
| nqueens                    | 117 ms                                                 | 123 ms: 1.06x slower                                                   |
| deepcopy_reduce            | 4.04 us                                                | 4.27 us: 1.06x slower                                                  |
| generators                 | 41.1 ms                                                | 43.6 ms: 1.06x slower                                                  |
| html5lib                   | 88.9 ms                                                | 94.8 ms: 1.07x slower                                                  |
| sympy_integrate            | 29.8 ms                                                | 31.8 ms: 1.07x slower                                                  |
| xml_etree_generate         | 127 ms                                                 | 136 ms: 1.07x slower                                                   |
| json                       | 6.85 ms                                                | 7.31 ms: 1.07x slower                                                  |
| tomli_loads                | 2.88 sec                                               | 3.11 sec: 1.08x slower                                                 |
| go                         | 172 ms                                                 | 187 ms: 1.09x slower                                                   |
| sympy_sum                  | 222 ms                                                 | 241 ms: 1.09x slower                                                   |
| pprint_pformat             | 1.98 sec                                               | 2.16 sec: 1.09x slower                                                 |
| 2to3                       | 456 ms                                                 | 506 ms: 1.11x slower                                                   |
| asyncio_tcp                | 923 ms                                                 | 1.02 sec: 1.11x slower                                                 |
| scimark_fft                | 500 ms                                                 | 556 ms: 1.11x slower                                                   |
| pprint_safe_repr           | 967 ms                                                 | 1.08 sec: 1.12x slower                                                 |
| meteor_contest             | 146 ms                                                 | 164 ms: 1.12x slower                                                   |
| unpickle                   | 21.2 us                                                | 23.9 us: 1.12x slower                                                  |
| hexiom                     | 8.27 ms                                                | 9.33 ms: 1.13x slower                                                  |
| genshi_xml                 | 67.6 ms                                                | 76.8 ms: 1.14x slower                                                  |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.21 sec: 1.14x slower                                                 |
| json_loads                 | 37.9 us                                                | 43.6 us: 1.15x slower                                                  |
| json_dumps                 | 14.3 ms                                                | 16.5 ms: 1.15x slower                                                  |
| xml_etree_process          | 83.7 ms                                                | 96.9 ms: 1.16x slower                                                  |
| pickle_pure_python         | 436 us                                                 | 506 us: 1.16x slower                                                   |
| django_template            | 44.9 ms                                                | 52.4 ms: 1.17x slower                                                  |
| sympy_str                  | 385 ms                                                 | 449 ms: 1.17x slower                                                   |
| scimark_monte_carlo        | 96.4 ms                                                | 113 ms: 1.17x slower                                                   |
| logging_format             | 9.59 us                                                | 11.3 us: 1.18x slower                                                  |
| richards                   | 60.3 ms                                                | 71.3 ms: 1.18x slower                                                  |
| richards_super             | 72.8 ms                                                | 86.6 ms: 1.19x slower                                                  |
| unpickle_list              | 6.83 us                                                | 8.15 us: 1.19x slower                                                  |
| scimark_lu                 | 152 ms                                                 | 181 ms: 1.19x slower                                                   |
| unpickle_pure_python       | 300 us                                                 | 358 us: 1.20x slower                                                   |
| fannkuch                   | 540 ms                                                 | 648 ms: 1.20x slower                                                   |
| sympy_expand               | 582 ms                                                 | 699 ms: 1.20x slower                                                   |
| thrift                     | 1.06 ms                                                | 1.28 ms: 1.21x slower                                                  |
| python_startup_no_site     | 17.6 ms                                                | 21.4 ms: 1.21x slower                                                  |
| genshi_text                | 30.2 ms                                                | 36.8 ms: 1.22x slower                                                  |
| python_startup             | 23.7 ms                                                | 29.4 ms: 1.24x slower                                                  |
| deltablue                  | 4.27 ms                                                | 5.40 ms: 1.26x slower                                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 8.47 ms: 1.26x slower                                                  |
| typing_runtime_protocols   | 224 us                                                 | 289 us: 1.29x slower                                                   |
| unpack_sequence            | 60.2 ns                                                | 78.0 ns: 1.30x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 2.55 ms: 1.32x slower                                                  |
| sqlalchemy_imperative      | 24.7 ms                                                | 33.1 ms: 1.34x slower                                                  |
| nbody                      | 119 ms                                                 | 167 ms: 1.40x slower                                                   |
| telco                      | 9.59 ms                                                | 13.5 ms: 1.41x slower                                                  |
| mako                       | 15.7 ms                                                | 23.1 ms: 1.47x slower                                                  |
| coverage                   | 95.4 ms                                                | 156 ms: 1.64x slower                                                   |
| bench_mp_pool              | 20.7 ms                                                | 82.2 ms: 3.97x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.02x slower                                                           |

Benchmark hidden because not significant (14): dulwich_log, bench_thread_pool, sqlalchemy_declarative, pickle_list, docutils, pickle, regex_compile, mdp, coroutines, logging_silent, regex_dna, scimark_sor, sqlite_synth, regex_v8
Ignored benchmarks (11) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20250322-3.14.0a6+-bc26f95-NOGIL/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.004x faster

# HPT report

- Reliability score: 88.03% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.38x