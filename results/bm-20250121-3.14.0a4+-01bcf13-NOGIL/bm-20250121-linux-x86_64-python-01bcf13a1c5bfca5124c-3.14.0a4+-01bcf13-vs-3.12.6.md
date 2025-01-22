# Results vs. 3.12.6

- fork: python
- ref: 01bcf13a1c5bfca5124c
- machine: linux-x86_64
- commit hash: 01bcf13
- commit date: 2025-01-21
- overall geometric mean: 1.097x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 567 ms: 1.24x slower                                                   |
| docutils       | 4.00 sec                                               | 4.15 sec: 1.04x slower                                                 |
| html5lib       | 88.9 ms                                                | 115 ms: 1.30x slower                                                   |
| Geometric mean | (ref)                                                  | 1.19x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 830 ms: 2.33x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 988 ms: 1.87x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 396 ms: 1.78x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 544 ms: 1.71x faster                                                   |
| async_tree_none            | 741 ms                                                 | 438 ms: 1.69x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 587 ms: 1.66x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 786 ms: 1.40x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 845 ms: 1.28x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 807 ms: 1.08x slower                                                   |
| coroutines                 | 29.5 ms                                                | 37.4 ms: 1.27x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.42x faster                                                           |

Benchmark hidden because not significant (1): async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 105 ms: 1.17x faster                                                   |
| pidigits       | 250 ms                                                 | 241 ms: 1.04x faster                                                   |
| nbody          | 119 ms                                                 | 206 ms: 1.73x slower                                                   |
| Geometric mean | (ref)                                                  | 1.13x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.22 ms: 1.22x faster                                                  |
| regex_dna      | 278 ms                                                 | 300 ms: 1.08x slower                                                   |
| regex_compile  | 187 ms                                                 | 222 ms: 1.19x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x slower                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 169 ms                                                 | 152 ms: 1.11x faster                                                   |
| json_loads           | 37.9 us                                                | 40.8 us: 1.08x slower                                                  |
| tomli_loads          | 2.88 sec                                               | 3.22 sec: 1.12x slower                                                 |
| json_dumps           | 14.3 ms                                                | 16.4 ms: 1.15x slower                                                  |
| unpickle_pure_python | 300 us                                                 | 392 us: 1.31x slower                                                   |
| xml_etree_process    | 83.7 ms                                                | 110 ms: 1.31x slower                                                   |
| xml_etree_generate   | 127 ms                                                 | 167 ms: 1.32x slower                                                   |
| pickle_pure_python   | 436 us                                                 | 668 us: 1.53x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.17x slower                                                           |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 21.3 ms: 1.21x slower                                                  |
| python_startup         | 23.7 ms                                                | 34.9 ms: 1.47x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.34x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 44.9 ms                                                | 55.1 ms: 1.23x slower                                                  |
| genshi_text     | 30.2 ms                                                | 43.2 ms: 1.43x slower                                                  |
| mako            | 15.7 ms                                                | 22.8 ms: 1.45x slower                                                  |
| genshi_xml      | 67.6 ms                                                | 104 ms: 1.54x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.41x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 830 ms: 2.33x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 988 ms: 1.87x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 396 ms: 1.78x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 544 ms: 1.71x faster                                                   |
| async_tree_none            | 741 ms                                                 | 438 ms: 1.69x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 587 ms: 1.66x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 786 ms: 1.40x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 845 ms: 1.28x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.22 ms: 1.22x faster                                                  |
| float                      | 123 ms                                                 | 105 ms: 1.17x faster                                                   |
| xml_etree_iterparse        | 169 ms                                                 | 152 ms: 1.11x faster                                                   |
| pycparser                  | 1.79 sec                                               | 1.63 sec: 1.10x faster                                                 |
| pidigits                   | 250 ms                                                 | 241 ms: 1.04x faster                                                   |
| docutils                   | 4.00 sec                                               | 4.15 sec: 1.04x slower                                                 |
| logging_silent             | 139 ns                                                 | 146 ns: 1.05x slower                                                   |
| mdp                        | 3.97 sec                                               | 4.19 sec: 1.05x slower                                                 |
| sqlglot_normalize          | 157 ms                                                 | 169 ms: 1.07x slower                                                   |
| regex_dna                  | 278 ms                                                 | 300 ms: 1.08x slower                                                   |
| json_loads                 | 37.9 us                                                | 40.8 us: 1.08x slower                                                  |
| asyncio_websockets         | 748 ms                                                 | 807 ms: 1.08x slower                                                   |
| scimark_sor                | 167 ms                                                 | 181 ms: 1.09x slower                                                   |
| comprehensions             | 27.1 us                                                | 29.5 us: 1.09x slower                                                  |
| tomli_loads                | 2.88 sec                                               | 3.22 sec: 1.12x slower                                                 |
| logging_simple             | 9.45 us                                                | 10.6 us: 1.13x slower                                                  |
| json                       | 6.85 ms                                                | 7.74 ms: 1.13x slower                                                  |
| raytrace                   | 408 ms                                                 | 463 ms: 1.14x slower                                                   |
| deepcopy                   | 468 us                                                 | 533 us: 1.14x slower                                                   |
| json_dumps                 | 14.3 ms                                                | 16.4 ms: 1.15x slower                                                  |
| scimark_fft                | 500 ms                                                 | 578 ms: 1.16x slower                                                   |
| richards_super             | 72.8 ms                                                | 84.5 ms: 1.16x slower                                                  |
| bench_thread_pool          | 3.48 ms                                                | 4.04 ms: 1.16x slower                                                  |
| deepcopy_reduce            | 4.04 us                                                | 4.70 us: 1.17x slower                                                  |
| nqueens                    | 117 ms                                                 | 137 ms: 1.17x slower                                                   |
| sqlglot_optimize           | 76.0 ms                                                | 89.5 ms: 1.18x slower                                                  |
| sympy_expand               | 582 ms                                                 | 686 ms: 1.18x slower                                                   |
| bpe_tokeniser              | 6.59 sec                                               | 7.77 sec: 1.18x slower                                                 |
| regex_compile              | 187 ms                                                 | 222 ms: 1.19x slower                                                   |
| richards                   | 60.3 ms                                                | 72.1 ms: 1.20x slower                                                  |
| crypto_pyaes               | 107 ms                                                 | 129 ms: 1.20x slower                                                   |
| generators                 | 41.1 ms                                                | 49.6 ms: 1.21x slower                                                  |
| python_startup_no_site     | 17.6 ms                                                | 21.3 ms: 1.21x slower                                                  |
| sympy_integrate            | 29.8 ms                                                | 36.1 ms: 1.21x slower                                                  |
| pprint_safe_repr           | 967 ms                                                 | 1.18 sec: 1.22x slower                                                 |
| fannkuch                   | 540 ms                                                 | 659 ms: 1.22x slower                                                   |
| django_template            | 44.9 ms                                                | 55.1 ms: 1.23x slower                                                  |
| dulwich_log                | 100 ms                                                 | 123 ms: 1.23x slower                                                   |
| pprint_pformat             | 1.98 sec                                               | 2.44 sec: 1.23x slower                                                 |
| scimark_monte_carlo        | 96.4 ms                                                | 119 ms: 1.24x slower                                                   |
| 2to3                       | 456 ms                                                 | 567 ms: 1.24x slower                                                   |
| logging_format             | 9.59 us                                                | 11.9 us: 1.24x slower                                                  |
| pyflate                    | 727 ms                                                 | 906 ms: 1.25x slower                                                   |
| sympy_str                  | 385 ms                                                 | 480 ms: 1.25x slower                                                   |
| meteor_contest             | 146 ms                                                 | 185 ms: 1.26x slower                                                   |
| coroutines                 | 29.5 ms                                                | 37.4 ms: 1.27x slower                                                  |
| sqlglot_transpile          | 2.34 ms                                                | 2.98 ms: 1.28x slower                                                  |
| html5lib                   | 88.9 ms                                                | 115 ms: 1.30x slower                                                   |
| sympy_sum                  | 222 ms                                                 | 288 ms: 1.30x slower                                                   |
| chaos                      | 84.9 ms                                                | 110 ms: 1.30x slower                                                   |
| unpickle_pure_python       | 300 us                                                 | 392 us: 1.31x slower                                                   |
| xml_etree_process          | 83.7 ms                                                | 110 ms: 1.31x slower                                                   |
| xml_etree_generate         | 127 ms                                                 | 167 ms: 1.32x slower                                                   |
| go                         | 172 ms                                                 | 227 ms: 1.32x slower                                                   |
| hexiom                     | 8.27 ms                                                | 11.0 ms: 1.33x slower                                                  |
| scimark_lu                 | 152 ms                                                 | 206 ms: 1.35x slower                                                   |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 9.10 ms: 1.36x slower                                                  |
| thrift                     | 1.06 ms                                                | 1.48 ms: 1.40x slower                                                  |
| sqlalchemy_imperative      | 24.7 ms                                                | 34.6 ms: 1.40x slower                                                  |
| telco                      | 9.59 ms                                                | 13.6 ms: 1.42x slower                                                  |
| gc_traversal               | 5.86 ms                                                | 8.35 ms: 1.42x slower                                                  |
| sqlglot_parse              | 1.79 ms                                                | 2.55 ms: 1.42x slower                                                  |
| genshi_text                | 30.2 ms                                                | 43.2 ms: 1.43x slower                                                  |
| mako                       | 15.7 ms                                                | 22.8 ms: 1.45x slower                                                  |
| typing_runtime_protocols   | 224 us                                                 | 327 us: 1.46x slower                                                   |
| python_startup             | 23.7 ms                                                | 34.9 ms: 1.47x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 2.95 ms: 1.52x slower                                                  |
| pickle_pure_python         | 436 us                                                 | 668 us: 1.53x slower                                                   |
| genshi_xml                 | 67.6 ms                                                | 104 ms: 1.54x slower                                                   |
| coverage                   | 95.4 ms                                                | 155 ms: 1.62x slower                                                   |
| deltablue                  | 4.27 ms                                                | 7.05 ms: 1.65x slower                                                  |
| nbody                      | 119 ms                                                 | 206 ms: 1.73x slower                                                   |
| bench_mp_pool              | 20.7 ms                                                | 92.5 ms: 4.47x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.15x slower                                                           |

Benchmark hidden because not significant (9): xml_etree_parse, async_generators, pathlib, regex_v8, deepcopy_memo, spectral_norm, pylint, sqlite_synth, sqlalchemy_declarative
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250121-3.14.0a4+-01bcf13-NOGIL/bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.097x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.35x