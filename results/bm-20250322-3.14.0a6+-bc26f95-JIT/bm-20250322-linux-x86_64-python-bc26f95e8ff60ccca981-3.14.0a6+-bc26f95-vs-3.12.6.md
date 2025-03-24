# Results vs. 3.12.6

- fork: python
- ref: bc26f95e8ff60ccca981
- machine: linux-x86_64
- commit hash: bc26f95
- commit date: 2025-03-22
- overall geometric mean: 1.135x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 4.00 sec                                               | 3.70 sec: 1.08x faster                                                 |
| Geometric mean | (ref)                                                  | 1.06x faster                                                           |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 889 ms: 2.18x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 863 ms: 2.14x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 471 ms: 2.08x faster                                                   |
| async_tree_none            | 741 ms                                                 | 360 ms: 2.06x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 460 ms: 2.02x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 354 ms: 1.99x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 645 ms: 1.71x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 695 ms: 1.55x faster                                                   |
| async_generators           | 589 ms                                                 | 518 ms: 1.14x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 705 ms: 1.06x faster                                                   |
| asyncio_tcp_ssl            | 2.81 sec                                               | 2.74 sec: 1.03x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.54x faster                                                           |

Benchmark hidden because not significant (2): asyncio_tcp, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 89.9 ms: 1.37x faster                                                  |
| nbody          | 119 ms                                                 | 111 ms: 1.08x faster                                                   |
| pidigits       | 250 ms                                                 | 237 ms: 1.05x faster                                                   |
| Geometric mean | (ref)                                                  | 1.16x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.50 ms: 1.14x faster                                                  |
| regex_compile  | 187 ms                                                 | 171 ms: 1.09x faster                                                   |
| regex_v8       | 32.5 ms                                                | 30.8 ms: 1.05x faster                                                  |
| Geometric mean | (ref)                                                  | 1.07x faster                                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_dict          | 52.7 us                                                | 41.0 us: 1.29x faster                                                  |
| xml_etree_iterparse  | 169 ms                                                 | 136 ms: 1.25x faster                                                   |
| xml_etree_parse      | 241 ms                                                 | 193 ms: 1.25x faster                                                   |
| tomli_loads          | 2.88 sec                                               | 2.39 sec: 1.20x faster                                                 |
| pickle_list          | 6.97 us                                                | 6.11 us: 1.14x faster                                                  |
| xml_etree_generate   | 127 ms                                                 | 116 ms: 1.10x faster                                                   |
| xml_etree_process    | 83.7 ms                                                | 76.6 ms: 1.09x faster                                                  |
| unpickle             | 21.2 us                                                | 19.7 us: 1.08x faster                                                  |
| unpickle_pure_python | 300 us                                                 | 281 us: 1.06x faster                                                   |
| json_dumps           | 14.3 ms                                                | 14.9 ms: 1.04x slower                                                  |
| pickle               | 16.4 us                                                | 17.2 us: 1.05x slower                                                  |
| unpickle_list        | 6.83 us                                                | 7.32 us: 1.07x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.09x faster                                                           |

Benchmark hidden because not significant (2): pickle_pure_python, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 16.7 ms: 1.05x faster                                                  |
| python_startup         | 23.7 ms                                                | 28.1 ms: 1.18x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.06x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text    | 30.2 ms                                                | 28.3 ms: 1.07x faster                                                  |
| genshi_xml     | 67.6 ms                                                | 73.1 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (2): mako, django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 889 ms: 2.18x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 863 ms: 2.14x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 471 ms: 2.08x faster                                                   |
| async_tree_none            | 741 ms                                                 | 360 ms: 2.06x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 460 ms: 2.02x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 354 ms: 1.99x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 645 ms: 1.71x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 695 ms: 1.55x faster                                                   |
| deepcopy                   | 468 us                                                 | 334 us: 1.40x faster                                                   |
| deepcopy_memo              | 52.4 us                                                | 37.8 us: 1.39x faster                                                  |
| float                      | 123 ms                                                 | 89.9 ms: 1.37x faster                                                  |
| sqlalchemy_declarative     | 218 ms                                                 | 169 ms: 1.29x faster                                                   |
| pickle_dict                | 52.7 us                                                | 41.0 us: 1.29x faster                                                  |
| richards                   | 60.3 ms                                                | 47.2 ms: 1.28x faster                                                  |
| spectral_norm              | 156 ms                                                 | 122 ms: 1.28x faster                                                   |
| scimark_fft                | 500 ms                                                 | 392 ms: 1.27x faster                                                   |
| xml_etree_iterparse        | 169 ms                                                 | 136 ms: 1.25x faster                                                   |
| xml_etree_parse            | 241 ms                                                 | 193 ms: 1.25x faster                                                   |
| logging_simple             | 9.45 us                                                | 7.62 us: 1.24x faster                                                  |
| dulwich_log                | 100 ms                                                 | 82.2 ms: 1.22x faster                                                  |
| tomli_loads                | 2.88 sec                                               | 2.39 sec: 1.20x faster                                                 |
| richards_super             | 72.8 ms                                                | 61.1 ms: 1.19x faster                                                  |
| comprehensions             | 27.1 us                                                | 23.0 us: 1.18x faster                                                  |
| deepcopy_reduce            | 4.04 us                                                | 3.44 us: 1.17x faster                                                  |
| pycparser                  | 1.79 sec                                               | 1.54 sec: 1.16x faster                                                 |
| pyflate                    | 727 ms                                                 | 626 ms: 1.16x faster                                                   |
| logging_silent             | 139 ns                                                 | 120 ns: 1.16x faster                                                   |
| raytrace                   | 408 ms                                                 | 352 ms: 1.16x faster                                                   |
| pylint                     | 465 ms                                                 | 403 ms: 1.15x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.50 ms: 1.14x faster                                                  |
| pickle_list                | 6.97 us                                                | 6.11 us: 1.14x faster                                                  |
| sympy_integrate            | 29.8 ms                                                | 26.1 ms: 1.14x faster                                                  |
| bpe_tokeniser              | 6.59 sec                                               | 5.78 sec: 1.14x faster                                                 |
| async_generators           | 589 ms                                                 | 518 ms: 1.14x faster                                                   |
| mdp                        | 3.97 sec                                               | 3.53 sec: 1.12x faster                                                 |
| crypto_pyaes               | 107 ms                                                 | 95.9 ms: 1.12x faster                                                  |
| deltablue                  | 4.27 ms                                                | 3.84 ms: 1.11x faster                                                  |
| sympy_sum                  | 222 ms                                                 | 200 ms: 1.11x faster                                                   |
| sqlite_synth               | 3.87 us                                                | 3.50 us: 1.11x faster                                                  |
| scimark_sor                | 167 ms                                                 | 151 ms: 1.10x faster                                                   |
| xml_etree_generate         | 127 ms                                                 | 116 ms: 1.10x faster                                                   |
| regex_compile              | 187 ms                                                 | 171 ms: 1.09x faster                                                   |
| xml_etree_process          | 83.7 ms                                                | 76.6 ms: 1.09x faster                                                  |
| chaos                      | 84.9 ms                                                | 77.8 ms: 1.09x faster                                                  |
| sympy_str                  | 385 ms                                                 | 355 ms: 1.08x faster                                                   |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 6.20 ms: 1.08x faster                                                  |
| unpickle                   | 21.2 us                                                | 19.7 us: 1.08x faster                                                  |
| docutils                   | 4.00 sec                                               | 3.70 sec: 1.08x faster                                                 |
| pathlib                    | 31.6 ms                                                | 29.3 ms: 1.08x faster                                                  |
| nbody                      | 119 ms                                                 | 111 ms: 1.08x faster                                                   |
| scimark_monte_carlo        | 96.4 ms                                                | 90.0 ms: 1.07x faster                                                  |
| genshi_text                | 30.2 ms                                                | 28.3 ms: 1.07x faster                                                  |
| unpickle_pure_python       | 300 us                                                 | 281 us: 1.06x faster                                                   |
| meteor_contest             | 146 ms                                                 | 138 ms: 1.06x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 705 ms: 1.06x faster                                                   |
| regex_v8                   | 32.5 ms                                                | 30.8 ms: 1.05x faster                                                  |
| python_startup_no_site     | 17.6 ms                                                | 16.7 ms: 1.05x faster                                                  |
| pidigits                   | 250 ms                                                 | 237 ms: 1.05x faster                                                   |
| go                         | 172 ms                                                 | 165 ms: 1.05x faster                                                   |
| asyncio_tcp_ssl            | 2.81 sec                                               | 2.74 sec: 1.03x faster                                                 |
| json_dumps                 | 14.3 ms                                                | 14.9 ms: 1.04x slower                                                  |
| sympy_expand               | 582 ms                                                 | 611 ms: 1.05x slower                                                   |
| pickle                     | 16.4 us                                                | 17.2 us: 1.05x slower                                                  |
| telco                      | 9.59 ms                                                | 10.2 ms: 1.06x slower                                                  |
| unpickle_list              | 6.83 us                                                | 7.32 us: 1.07x slower                                                  |
| genshi_xml                 | 67.6 ms                                                | 73.1 ms: 1.08x slower                                                  |
| coverage                   | 95.4 ms                                                | 107 ms: 1.12x slower                                                   |
| hexiom                     | 8.27 ms                                                | 9.43 ms: 1.14x slower                                                  |
| python_startup             | 23.7 ms                                                | 28.1 ms: 1.18x slower                                                  |
| unpack_sequence            | 60.2 ns                                                | 72.2 ns: 1.20x slower                                                  |
| gc_traversal               | 5.86 ms                                                | 8.00 ms: 1.36x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 3.62 ms: 1.87x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 93.5 ms: 4.52x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.11x faster                                                           |

Benchmark hidden because not significant (20): bench_thread_pool, 2to3, logging_format, nqueens, fannkuch, pickle_pure_python, sqlalchemy_imperative, scimark_lu, json, asyncio_tcp, pprint_safe_repr, generators, typing_runtime_protocols, coroutines, json_loads, thrift, mako, pprint_pformat, regex_dna, django_template
Ignored benchmarks (12) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20250322-3.14.0a6+-bc26f95-JIT/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.135x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.16x