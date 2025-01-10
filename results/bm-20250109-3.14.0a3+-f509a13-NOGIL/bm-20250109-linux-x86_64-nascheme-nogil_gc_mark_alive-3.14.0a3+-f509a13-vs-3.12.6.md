# Results vs. 3.12.6

- fork: nascheme
- ref: nogil_gc_mark_alive
- machine: linux-x86_64
- commit hash: f509a13
- commit date: 2025-01-09
- overall geometric mean: 1.184x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 681 ms: 1.49x slower                                                    |
| docutils       | 4.00 sec                                               | 4.92 sec: 1.23x slower                                                  |
| html5lib       | 88.9 ms                                                | 129 ms: 1.45x slower                                                    |
| Geometric mean | (ref)                                                  | 1.39x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.04 sec: 1.87x faster                                                  |
| async_tree_io              | 1.85 sec                                               | 1.14 sec: 1.63x faster                                                  |
| async_tree_none_tg         | 704 ms                                                 | 436 ms: 1.61x faster                                                    |
| async_tree_memoization_tg  | 930 ms                                                 | 577 ms: 1.61x faster                                                    |
| async_tree_memoization     | 977 ms                                                 | 652 ms: 1.50x faster                                                    |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 816 ms: 1.32x faster                                                    |
| async_tree_none            | 741 ms                                                 | 565 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 860 ms: 1.28x faster                                                    |
| asyncio_websockets         | 748 ms                                                 | 830 ms: 1.11x slower                                                    |
| async_generators           | 589 ms                                                 | 665 ms: 1.13x slower                                                    |
| coroutines                 | 29.5 ms                                                | 37.4 ms: 1.27x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.29x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 250 ms                                                 | 236 ms: 1.06x faster                                                    |
| float          | 123 ms                                                 | 146 ms: 1.19x slower                                                    |
| nbody          | 119 ms                                                 | 197 ms: 1.65x slower                                                    |
| Geometric mean | (ref)                                                  | 1.23x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.84 ms: 1.06x faster                                                   |
| regex_v8       | 32.5 ms                                                | 34.8 ms: 1.07x slower                                                   |
| regex_compile  | 187 ms                                                 | 234 ms: 1.25x slower                                                    |
| Geometric mean | (ref)                                                  | 1.06x slower                                                            |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 169 ms                                                 | 151 ms: 1.12x faster                                                    |
| xml_etree_parse      | 241 ms                                                 | 256 ms: 1.06x slower                                                    |
| json_loads           | 37.9 us                                                | 41.7 us: 1.10x slower                                                   |
| tomli_loads          | 2.88 sec                                               | 3.23 sec: 1.12x slower                                                  |
| xml_etree_generate   | 127 ms                                                 | 145 ms: 1.14x slower                                                    |
| xml_etree_process    | 83.7 ms                                                | 108 ms: 1.29x slower                                                    |
| json_dumps           | 14.3 ms                                                | 19.0 ms: 1.33x slower                                                   |
| unpickle_pure_python | 300 us                                                 | 468 us: 1.56x slower                                                    |
| pickle_pure_python   | 436 us                                                 | 813 us: 1.87x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.23x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 27.2 ms: 1.55x slower                                                   |
| python_startup         | 23.7 ms                                                | 42.9 ms: 1.81x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.67x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| django_template | 44.9 ms                                                | 61.3 ms: 1.36x slower                                                   |
| genshi_text     | 30.2 ms                                                | 43.1 ms: 1.43x slower                                                   |
| genshi_xml      | 67.6 ms                                                | 97.3 ms: 1.44x slower                                                   |
| mako            | 15.7 ms                                                | 27.5 ms: 1.75x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.49x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.04 sec: 1.87x faster                                                  |
| async_tree_io              | 1.85 sec                                               | 1.14 sec: 1.63x faster                                                  |
| async_tree_none_tg         | 704 ms                                                 | 436 ms: 1.61x faster                                                    |
| async_tree_memoization_tg  | 930 ms                                                 | 577 ms: 1.61x faster                                                    |
| async_tree_memoization     | 977 ms                                                 | 652 ms: 1.50x faster                                                    |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 816 ms: 1.32x faster                                                    |
| async_tree_none            | 741 ms                                                 | 565 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 860 ms: 1.28x faster                                                    |
| xml_etree_iterparse        | 169 ms                                                 | 151 ms: 1.12x faster                                                    |
| regex_effbot               | 5.13 ms                                                | 4.84 ms: 1.06x faster                                                   |
| pidigits                   | 250 ms                                                 | 236 ms: 1.06x faster                                                    |
| xml_etree_parse            | 241 ms                                                 | 256 ms: 1.06x slower                                                    |
| pathlib                    | 31.6 ms                                                | 33.7 ms: 1.07x slower                                                   |
| regex_v8                   | 32.5 ms                                                | 34.8 ms: 1.07x slower                                                   |
| sqlite_synth               | 3.87 us                                                | 4.22 us: 1.09x slower                                                   |
| json_loads                 | 37.9 us                                                | 41.7 us: 1.10x slower                                                   |
| pycparser                  | 1.79 sec                                               | 1.98 sec: 1.10x slower                                                  |
| asyncio_websockets         | 748 ms                                                 | 830 ms: 1.11x slower                                                    |
| sqlglot_normalize          | 157 ms                                                 | 175 ms: 1.11x slower                                                    |
| tomli_loads                | 2.88 sec                                               | 3.23 sec: 1.12x slower                                                  |
| scimark_fft                | 500 ms                                                 | 563 ms: 1.13x slower                                                    |
| async_generators           | 589 ms                                                 | 665 ms: 1.13x slower                                                    |
| deepcopy_memo              | 52.4 us                                                | 59.6 us: 1.14x slower                                                   |
| xml_etree_generate         | 127 ms                                                 | 145 ms: 1.14x slower                                                    |
| deepcopy_reduce            | 4.04 us                                                | 4.63 us: 1.15x slower                                                   |
| pylint                     | 465 ms                                                 | 540 ms: 1.16x slower                                                    |
| json                       | 6.85 ms                                                | 7.98 ms: 1.17x slower                                                   |
| float                      | 123 ms                                                 | 146 ms: 1.19x slower                                                    |
| mdp                        | 3.97 sec                                               | 4.86 sec: 1.22x slower                                                  |
| docutils                   | 4.00 sec                                               | 4.92 sec: 1.23x slower                                                  |
| telco                      | 9.59 ms                                                | 11.9 ms: 1.24x slower                                                   |
| nqueens                    | 117 ms                                                 | 145 ms: 1.24x slower                                                    |
| crypto_pyaes               | 107 ms                                                 | 134 ms: 1.25x slower                                                    |
| regex_compile              | 187 ms                                                 | 234 ms: 1.25x slower                                                    |
| sqlglot_optimize           | 76.0 ms                                                | 95.7 ms: 1.26x slower                                                   |
| pyflate                    | 727 ms                                                 | 917 ms: 1.26x slower                                                    |
| coroutines                 | 29.5 ms                                                | 37.4 ms: 1.27x slower                                                   |
| fannkuch                   | 540 ms                                                 | 691 ms: 1.28x slower                                                    |
| sympy_expand               | 582 ms                                                 | 750 ms: 1.29x slower                                                    |
| sympy_integrate            | 29.8 ms                                                | 38.5 ms: 1.29x slower                                                   |
| xml_etree_process          | 83.7 ms                                                | 108 ms: 1.29x slower                                                    |
| typing_runtime_protocols   | 224 us                                                 | 290 us: 1.29x slower                                                    |
| thrift                     | 1.06 ms                                                | 1.39 ms: 1.31x slower                                                   |
| scimark_lu                 | 152 ms                                                 | 200 ms: 1.32x slower                                                    |
| sympy_sum                  | 222 ms                                                 | 292 ms: 1.32x slower                                                    |
| json_dumps                 | 14.3 ms                                                | 19.0 ms: 1.33x slower                                                   |
| pprint_pformat             | 1.98 sec                                               | 2.64 sec: 1.33x slower                                                  |
| comprehensions             | 27.1 us                                                | 36.2 us: 1.34x slower                                                   |
| meteor_contest             | 146 ms                                                 | 196 ms: 1.34x slower                                                    |
| bpe_tokeniser              | 6.59 sec                                               | 8.87 sec: 1.35x slower                                                  |
| sympy_str                  | 385 ms                                                 | 520 ms: 1.35x slower                                                    |
| generators                 | 41.1 ms                                                | 56.0 ms: 1.36x slower                                                   |
| django_template            | 44.9 ms                                                | 61.3 ms: 1.36x slower                                                   |
| richards_super             | 72.8 ms                                                | 99.6 ms: 1.37x slower                                                   |
| logging_format             | 9.59 us                                                | 13.2 us: 1.37x slower                                                   |
| scimark_monte_carlo        | 96.4 ms                                                | 133 ms: 1.38x slower                                                    |
| logging_simple             | 9.45 us                                                | 13.1 us: 1.39x slower                                                   |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 9.34 ms: 1.39x slower                                                   |
| pprint_safe_repr           | 967 ms                                                 | 1.36 sec: 1.41x slower                                                  |
| genshi_text                | 30.2 ms                                                | 43.1 ms: 1.43x slower                                                   |
| genshi_xml                 | 67.6 ms                                                | 97.3 ms: 1.44x slower                                                   |
| html5lib                   | 88.9 ms                                                | 129 ms: 1.45x slower                                                    |
| richards                   | 60.3 ms                                                | 88.2 ms: 1.46x slower                                                   |
| scimark_sor                | 167 ms                                                 | 247 ms: 1.48x slower                                                    |
| coverage                   | 95.4 ms                                                | 142 ms: 1.49x slower                                                    |
| 2to3                       | 456 ms                                                 | 681 ms: 1.49x slower                                                    |
| sqlalchemy_declarative     | 218 ms                                                 | 325 ms: 1.49x slower                                                    |
| hexiom                     | 8.27 ms                                                | 12.4 ms: 1.50x slower                                                   |
| sqlalchemy_imperative      | 24.7 ms                                                | 37.2 ms: 1.51x slower                                                   |
| python_startup_no_site     | 17.6 ms                                                | 27.2 ms: 1.55x slower                                                   |
| dulwich_log                | 100 ms                                                 | 155 ms: 1.55x slower                                                    |
| unpickle_pure_python       | 300 us                                                 | 468 us: 1.56x slower                                                    |
| raytrace                   | 408 ms                                                 | 644 ms: 1.58x slower                                                    |
| chaos                      | 84.9 ms                                                | 138 ms: 1.62x slower                                                    |
| nbody                      | 119 ms                                                 | 197 ms: 1.65x slower                                                    |
| bench_thread_pool          | 3.48 ms                                                | 5.81 ms: 1.67x slower                                                   |
| logging_silent             | 139 ns                                                 | 233 ns: 1.67x slower                                                    |
| gc_traversal               | 5.86 ms                                                | 10.2 ms: 1.73x slower                                                   |
| sqlglot_parse              | 1.79 ms                                                | 3.12 ms: 1.74x slower                                                   |
| mako                       | 15.7 ms                                                | 27.5 ms: 1.75x slower                                                   |
| sqlglot_transpile          | 2.34 ms                                                | 4.15 ms: 1.78x slower                                                   |
| python_startup             | 23.7 ms                                                | 42.9 ms: 1.81x slower                                                   |
| go                         | 172 ms                                                 | 314 ms: 1.83x slower                                                    |
| pickle_pure_python         | 436 us                                                 | 813 us: 1.87x slower                                                    |
| create_gc_cycles           | 1.94 ms                                                | 3.97 ms: 2.05x slower                                                   |
| deltablue                  | 4.27 ms                                                | 10.3 ms: 2.42x slower                                                   |
| bench_mp_pool              | 20.7 ms                                                | 101 ms: 4.89x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.27x slower                                                            |

Benchmark hidden because not significant (3): regex_dna, deepcopy, spectral_norm
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250109-3.14.0a3+-f509a13-NOGIL/bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.184x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.20x
- 95% likely to have a slowdown of 1.19x
- 99% likely to have a slowdown of 1.15x

# Memory
- memory change: 1.34x