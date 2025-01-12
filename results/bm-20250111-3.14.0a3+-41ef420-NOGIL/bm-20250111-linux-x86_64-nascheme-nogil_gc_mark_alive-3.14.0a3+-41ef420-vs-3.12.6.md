# Results vs. 3.12.6

- fork: nascheme
- ref: nogil_gc_mark_alive
- machine: linux-x86_64
- commit hash: 41ef420
- commit date: 2025-01-11
- overall geometric mean: 1.175x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 660 ms: 1.45x slower                                                    |
| docutils       | 4.00 sec                                               | 4.79 sec: 1.20x slower                                                  |
| html5lib       | 88.9 ms                                                | 133 ms: 1.49x slower                                                    |
| Geometric mean | (ref)                                                  | 1.37x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 996 ms: 1.94x faster                                                    |
| async_tree_io              | 1.85 sec                                               | 1.12 sec: 1.64x faster                                                  |
| async_tree_none_tg         | 704 ms                                                 | 445 ms: 1.58x faster                                                    |
| async_tree_memoization_tg  | 930 ms                                                 | 645 ms: 1.44x faster                                                    |
| async_tree_none            | 741 ms                                                 | 535 ms: 1.39x faster                                                    |
| async_tree_memoization     | 977 ms                                                 | 705 ms: 1.39x faster                                                    |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 806 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 849 ms: 1.27x faster                                                    |
| asyncio_websockets         | 748 ms                                                 | 827 ms: 1.11x slower                                                    |
| async_generators           | 589 ms                                                 | 681 ms: 1.16x slower                                                    |
| coroutines                 | 29.5 ms                                                | 38.7 ms: 1.31x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.28x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 250 ms                                                 | 236 ms: 1.06x faster                                                    |
| float          | 123 ms                                                 | 151 ms: 1.22x slower                                                    |
| nbody          | 119 ms                                                 | 177 ms: 1.49x slower                                                    |
| Geometric mean | (ref)                                                  | 1.20x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.49 ms: 1.14x faster                                                   |
| regex_dna      | 278 ms                                                 | 325 ms: 1.17x slower                                                    |
| regex_compile  | 187 ms                                                 | 256 ms: 1.37x slower                                                    |
| Geometric mean | (ref)                                                  | 1.10x slower                                                            |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 169 ms                                                 | 143 ms: 1.18x faster                                                    |
| xml_etree_parse      | 241 ms                                                 | 206 ms: 1.17x faster                                                    |
| tomli_loads          | 2.88 sec                                               | 3.20 sec: 1.11x slower                                                  |
| json_loads           | 37.9 us                                                | 43.1 us: 1.14x slower                                                   |
| xml_etree_generate   | 127 ms                                                 | 150 ms: 1.18x slower                                                    |
| json_dumps           | 14.3 ms                                                | 18.0 ms: 1.26x slower                                                   |
| xml_etree_process    | 83.7 ms                                                | 108 ms: 1.29x slower                                                    |
| pickle_pure_python   | 436 us                                                 | 615 us: 1.41x slower                                                    |
| unpickle_pure_python | 300 us                                                 | 475 us: 1.59x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.16x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 26.0 ms: 1.48x slower                                                   |
| python_startup         | 23.7 ms                                                | 36.2 ms: 1.53x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.50x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 89.7 ms: 1.33x slower                                                   |
| genshi_text     | 30.2 ms                                                | 41.6 ms: 1.38x slower                                                   |
| django_template | 44.9 ms                                                | 65.3 ms: 1.45x slower                                                   |
| mako            | 15.7 ms                                                | 25.5 ms: 1.62x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.44x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 996 ms: 1.94x faster                                                    |
| async_tree_io              | 1.85 sec                                               | 1.12 sec: 1.64x faster                                                  |
| async_tree_none_tg         | 704 ms                                                 | 445 ms: 1.58x faster                                                    |
| async_tree_memoization_tg  | 930 ms                                                 | 645 ms: 1.44x faster                                                    |
| async_tree_none            | 741 ms                                                 | 535 ms: 1.39x faster                                                    |
| async_tree_memoization     | 977 ms                                                 | 705 ms: 1.39x faster                                                    |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 806 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 849 ms: 1.27x faster                                                    |
| xml_etree_iterparse        | 169 ms                                                 | 143 ms: 1.18x faster                                                    |
| xml_etree_parse            | 241 ms                                                 | 206 ms: 1.17x faster                                                    |
| regex_effbot               | 5.13 ms                                                | 4.49 ms: 1.14x faster                                                   |
| pidigits                   | 250 ms                                                 | 236 ms: 1.06x faster                                                    |
| pycparser                  | 1.79 sec                                               | 1.86 sec: 1.04x slower                                                  |
| pathlib                    | 31.6 ms                                                | 33.5 ms: 1.06x slower                                                   |
| pylint                     | 465 ms                                                 | 498 ms: 1.07x slower                                                    |
| deepcopy_memo              | 52.4 us                                                | 57.4 us: 1.10x slower                                                   |
| scimark_fft                | 500 ms                                                 | 549 ms: 1.10x slower                                                    |
| asyncio_websockets         | 748 ms                                                 | 827 ms: 1.11x slower                                                    |
| tomli_loads                | 2.88 sec                                               | 3.20 sec: 1.11x slower                                                  |
| spectral_norm              | 156 ms                                                 | 175 ms: 1.12x slower                                                    |
| json_loads                 | 37.9 us                                                | 43.1 us: 1.14x slower                                                   |
| nqueens                    | 117 ms                                                 | 134 ms: 1.15x slower                                                    |
| sqlglot_normalize          | 157 ms                                                 | 180 ms: 1.15x slower                                                    |
| async_generators           | 589 ms                                                 | 681 ms: 1.16x slower                                                    |
| regex_dna                  | 278 ms                                                 | 325 ms: 1.17x slower                                                    |
| xml_etree_generate         | 127 ms                                                 | 150 ms: 1.18x slower                                                    |
| dulwich_log                | 100 ms                                                 | 119 ms: 1.19x slower                                                    |
| docutils                   | 4.00 sec                                               | 4.79 sec: 1.20x slower                                                  |
| telco                      | 9.59 ms                                                | 11.6 ms: 1.21x slower                                                   |
| deepcopy_reduce            | 4.04 us                                                | 4.89 us: 1.21x slower                                                   |
| meteor_contest             | 146 ms                                                 | 178 ms: 1.22x slower                                                    |
| float                      | 123 ms                                                 | 151 ms: 1.22x slower                                                    |
| mdp                        | 3.97 sec                                               | 4.89 sec: 1.23x slower                                                  |
| crypto_pyaes               | 107 ms                                                 | 133 ms: 1.24x slower                                                    |
| json_dumps                 | 14.3 ms                                                | 18.0 ms: 1.26x slower                                                   |
| fannkuch                   | 540 ms                                                 | 684 ms: 1.27x slower                                                    |
| logging_format             | 9.59 us                                                | 12.2 us: 1.28x slower                                                   |
| pyflate                    | 727 ms                                                 | 928 ms: 1.28x slower                                                    |
| xml_etree_process          | 83.7 ms                                                | 108 ms: 1.29x slower                                                    |
| sqlglot_optimize           | 76.0 ms                                                | 98.4 ms: 1.29x slower                                                   |
| coroutines                 | 29.5 ms                                                | 38.7 ms: 1.31x slower                                                   |
| sympy_expand               | 582 ms                                                 | 762 ms: 1.31x slower                                                    |
| logging_simple             | 9.45 us                                                | 12.4 us: 1.31x slower                                                   |
| sympy_sum                  | 222 ms                                                 | 293 ms: 1.32x slower                                                    |
| scimark_lu                 | 152 ms                                                 | 201 ms: 1.32x slower                                                    |
| sqlalchemy_declarative     | 218 ms                                                 | 289 ms: 1.33x slower                                                    |
| genshi_xml                 | 67.6 ms                                                | 89.7 ms: 1.33x slower                                                   |
| sympy_str                  | 385 ms                                                 | 513 ms: 1.33x slower                                                    |
| bpe_tokeniser              | 6.59 sec                                               | 8.78 sec: 1.33x slower                                                  |
| sympy_integrate            | 29.8 ms                                                | 39.8 ms: 1.34x slower                                                   |
| regex_compile              | 187 ms                                                 | 256 ms: 1.37x slower                                                    |
| richards                   | 60.3 ms                                                | 83.0 ms: 1.38x slower                                                   |
| genshi_text                | 30.2 ms                                                | 41.6 ms: 1.38x slower                                                   |
| gc_traversal               | 5.86 ms                                                | 8.15 ms: 1.39x slower                                                   |
| coverage                   | 95.4 ms                                                | 133 ms: 1.40x slower                                                    |
| generators                 | 41.1 ms                                                | 57.7 ms: 1.40x slower                                                   |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 9.40 ms: 1.40x slower                                                   |
| pickle_pure_python         | 436 us                                                 | 615 us: 1.41x slower                                                    |
| pprint_pformat             | 1.98 sec                                               | 2.83 sec: 1.43x slower                                                  |
| 2to3                       | 456 ms                                                 | 660 ms: 1.45x slower                                                    |
| pprint_safe_repr           | 967 ms                                                 | 1.40 sec: 1.45x slower                                                  |
| django_template            | 44.9 ms                                                | 65.3 ms: 1.45x slower                                                   |
| typing_runtime_protocols   | 224 us                                                 | 326 us: 1.45x slower                                                    |
| comprehensions             | 27.1 us                                                | 39.7 us: 1.46x slower                                                   |
| python_startup_no_site     | 17.6 ms                                                | 26.0 ms: 1.48x slower                                                   |
| nbody                      | 119 ms                                                 | 177 ms: 1.49x slower                                                    |
| scimark_sor                | 167 ms                                                 | 249 ms: 1.49x slower                                                    |
| html5lib                   | 88.9 ms                                                | 133 ms: 1.49x slower                                                    |
| bench_thread_pool          | 3.48 ms                                                | 5.23 ms: 1.50x slower                                                   |
| thrift                     | 1.06 ms                                                | 1.60 ms: 1.51x slower                                                   |
| python_startup             | 23.7 ms                                                | 36.2 ms: 1.53x slower                                                   |
| scimark_monte_carlo        | 96.4 ms                                                | 148 ms: 1.54x slower                                                    |
| chaos                      | 84.9 ms                                                | 131 ms: 1.55x slower                                                    |
| go                         | 172 ms                                                 | 269 ms: 1.56x slower                                                    |
| sqlalchemy_imperative      | 24.7 ms                                                | 39.1 ms: 1.58x slower                                                   |
| unpickle_pure_python       | 300 us                                                 | 475 us: 1.59x slower                                                    |
| richards_super             | 72.8 ms                                                | 116 ms: 1.59x slower                                                    |
| logging_silent             | 139 ns                                                 | 222 ns: 1.59x slower                                                    |
| raytrace                   | 408 ms                                                 | 659 ms: 1.62x slower                                                    |
| mako                       | 15.7 ms                                                | 25.5 ms: 1.62x slower                                                   |
| sqlglot_transpile          | 2.34 ms                                                | 3.80 ms: 1.63x slower                                                   |
| hexiom                     | 8.27 ms                                                | 13.8 ms: 1.66x slower                                                   |
| create_gc_cycles           | 1.94 ms                                                | 3.45 ms: 1.78x slower                                                   |
| sqlglot_parse              | 1.79 ms                                                | 3.37 ms: 1.88x slower                                                   |
| deltablue                  | 4.27 ms                                                | 10.6 ms: 2.48x slower                                                   |
| bench_mp_pool              | 20.7 ms                                                | 96.3 ms: 4.65x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.25x slower                                                            |

Benchmark hidden because not significant (4): deepcopy, sqlite_synth, json, regex_v8
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250111-3.14.0a3+-41ef420-NOGIL/bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.175x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.20x
- 95% likely to have a slowdown of 1.18x
- 99% likely to have a slowdown of 1.16x

# Memory
- memory change: 1.34x