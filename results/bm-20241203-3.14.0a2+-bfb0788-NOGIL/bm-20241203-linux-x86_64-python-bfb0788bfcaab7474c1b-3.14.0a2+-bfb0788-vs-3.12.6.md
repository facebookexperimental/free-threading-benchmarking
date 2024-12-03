# Results vs. 3.12.6

- fork: python
- ref: bfb0788bfcaab7474c1b
- machine: linux-x86_64
- commit hash: bfb0788
- commit date: 2024-12-03
- overall geometric mean: 1.204x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 649 ms: 1.42x slower                                                   |
| docutils       | 4.00 sec                                               | 4.44 sec: 1.11x slower                                                 |
| html5lib       | 88.9 ms                                                | 124 ms: 1.40x slower                                                   |
| Geometric mean | (ref)                                                  | 1.30x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.10 sec: 1.76x faster                                                 |
| async_tree_memoization_tg  | 930 ms                                                 | 615 ms: 1.51x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 1.25 sec: 1.48x faster                                                 |
| async_tree_none_tg         | 704 ms                                                 | 488 ms: 1.44x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 681 ms: 1.43x faster                                                   |
| async_tree_none            | 741 ms                                                 | 559 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 853 ms: 1.29x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 867 ms: 1.24x faster                                                   |
| async_generators           | 589 ms                                                 | 709 ms: 1.20x slower                                                   |
| coroutines                 | 29.5 ms                                                | 38.6 ms: 1.31x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.24x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 250 ms                                                 | 242 ms: 1.03x faster                                                   |
| float          | 123 ms                                                 | 177 ms: 1.44x slower                                                   |
| nbody          | 119 ms                                                 | 195 ms: 1.64x slower                                                   |
| Geometric mean | (ref)                                                  | 1.32x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.35 ms: 1.18x faster                                                  |
| regex_v8       | 32.5 ms                                                | 34.6 ms: 1.06x slower                                                  |
| regex_dna      | 278 ms                                                 | 305 ms: 1.10x slower                                                   |
| regex_compile  | 187 ms                                                 | 244 ms: 1.31x slower                                                   |
| Geometric mean | (ref)                                                  | 1.07x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 169 ms                                                 | 134 ms: 1.26x faster                                                   |
| xml_etree_parse      | 241 ms                                                 | 195 ms: 1.24x faster                                                   |
| xml_etree_generate   | 127 ms                                                 | 148 ms: 1.16x slower                                                   |
| tomli_loads          | 2.88 sec                                               | 3.57 sec: 1.24x slower                                                 |
| xml_etree_process    | 83.7 ms                                                | 106 ms: 1.27x slower                                                   |
| json_dumps           | 14.3 ms                                                | 18.9 ms: 1.32x slower                                                  |
| pickle_pure_python   | 436 us                                                 | 686 us: 1.57x slower                                                   |
| unpickle_pure_python | 300 us                                                 | 476 us: 1.59x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.16x slower                                                           |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 20.3 ms: 1.15x slower                                                  |
| python_startup         | 23.7 ms                                                | 32.7 ms: 1.38x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.26x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 30.2 ms                                                | 43.4 ms: 1.44x slower                                                  |
| genshi_xml      | 67.6 ms                                                | 101 ms: 1.50x slower                                                   |
| django_template | 44.9 ms                                                | 71.0 ms: 1.58x slower                                                  |
| mako            | 15.7 ms                                                | 27.7 ms: 1.76x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.56x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.10 sec: 1.76x faster                                                 |
| async_tree_memoization_tg  | 930 ms                                                 | 615 ms: 1.51x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 1.25 sec: 1.48x faster                                                 |
| async_tree_none_tg         | 704 ms                                                 | 488 ms: 1.44x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 681 ms: 1.43x faster                                                   |
| async_tree_none            | 741 ms                                                 | 559 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 853 ms: 1.29x faster                                                   |
| xml_etree_iterparse        | 169 ms                                                 | 134 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 867 ms: 1.24x faster                                                   |
| xml_etree_parse            | 241 ms                                                 | 195 ms: 1.24x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.35 ms: 1.18x faster                                                  |
| deepcopy                   | 468 us                                                 | 438 us: 1.07x faster                                                   |
| pathlib                    | 31.6 ms                                                | 29.9 ms: 1.06x faster                                                  |
| pidigits                   | 250 ms                                                 | 242 ms: 1.03x faster                                                   |
| json                       | 6.85 ms                                                | 7.26 ms: 1.06x slower                                                  |
| regex_v8                   | 32.5 ms                                                | 34.6 ms: 1.06x slower                                                  |
| scimark_fft                | 500 ms                                                 | 539 ms: 1.08x slower                                                   |
| nqueens                    | 117 ms                                                 | 127 ms: 1.09x slower                                                   |
| regex_dna                  | 278 ms                                                 | 305 ms: 1.10x slower                                                   |
| docutils                   | 4.00 sec                                               | 4.44 sec: 1.11x slower                                                 |
| crypto_pyaes               | 107 ms                                                 | 120 ms: 1.12x slower                                                   |
| deepcopy_memo              | 52.4 us                                                | 59.4 us: 1.13x slower                                                  |
| pycparser                  | 1.79 sec                                               | 2.04 sec: 1.14x slower                                                 |
| spectral_norm              | 156 ms                                                 | 179 ms: 1.15x slower                                                   |
| python_startup_no_site     | 17.6 ms                                                | 20.3 ms: 1.15x slower                                                  |
| deepcopy_reduce            | 4.04 us                                                | 4.66 us: 1.16x slower                                                  |
| xml_etree_generate         | 127 ms                                                 | 148 ms: 1.16x slower                                                   |
| mdp                        | 3.97 sec                                               | 4.65 sec: 1.17x slower                                                 |
| meteor_contest             | 146 ms                                                 | 174 ms: 1.19x slower                                                   |
| dulwich_log                | 100 ms                                                 | 119 ms: 1.19x slower                                                   |
| async_generators           | 589 ms                                                 | 709 ms: 1.20x slower                                                   |
| pylint                     | 465 ms                                                 | 561 ms: 1.21x slower                                                   |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 8.09 ms: 1.21x slower                                                  |
| tomli_loads                | 2.88 sec                                               | 3.57 sec: 1.24x slower                                                 |
| bpe_tokeniser              | 6.59 sec                                               | 8.23 sec: 1.25x slower                                                 |
| sqlglot_normalize          | 157 ms                                                 | 198 ms: 1.26x slower                                                   |
| xml_etree_process          | 83.7 ms                                                | 106 ms: 1.27x slower                                                   |
| fannkuch                   | 540 ms                                                 | 687 ms: 1.27x slower                                                   |
| sqlglot_optimize           | 76.0 ms                                                | 96.8 ms: 1.27x slower                                                  |
| coroutines                 | 29.5 ms                                                | 38.6 ms: 1.31x slower                                                  |
| regex_compile              | 187 ms                                                 | 244 ms: 1.31x slower                                                   |
| generators                 | 41.1 ms                                                | 54.0 ms: 1.31x slower                                                  |
| json_dumps                 | 14.3 ms                                                | 18.9 ms: 1.32x slower                                                  |
| comprehensions             | 27.1 us                                                | 36.0 us: 1.33x slower                                                  |
| pyflate                    | 727 ms                                                 | 967 ms: 1.33x slower                                                   |
| typing_runtime_protocols   | 224 us                                                 | 300 us: 1.34x slower                                                   |
| sqlalchemy_declarative     | 218 ms                                                 | 296 ms: 1.36x slower                                                   |
| telco                      | 9.59 ms                                                | 13.1 ms: 1.36x slower                                                  |
| sympy_integrate            | 29.8 ms                                                | 40.7 ms: 1.37x slower                                                  |
| python_startup             | 23.7 ms                                                | 32.7 ms: 1.38x slower                                                  |
| pprint_safe_repr           | 967 ms                                                 | 1.34 sec: 1.39x slower                                                 |
| html5lib                   | 88.9 ms                                                | 124 ms: 1.40x slower                                                   |
| thrift                     | 1.06 ms                                                | 1.49 ms: 1.41x slower                                                  |
| 2to3                       | 456 ms                                                 | 649 ms: 1.42x slower                                                   |
| genshi_text                | 30.2 ms                                                | 43.4 ms: 1.44x slower                                                  |
| pprint_pformat             | 1.98 sec                                               | 2.84 sec: 1.44x slower                                                 |
| float                      | 123 ms                                                 | 177 ms: 1.44x slower                                                   |
| genshi_xml                 | 67.6 ms                                                | 101 ms: 1.50x slower                                                   |
| logging_simple             | 9.45 us                                                | 14.4 us: 1.52x slower                                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 148 ms: 1.54x slower                                                   |
| coverage                   | 95.4 ms                                                | 148 ms: 1.56x slower                                                   |
| richards_super             | 72.8 ms                                                | 115 ms: 1.57x slower                                                   |
| pickle_pure_python         | 436 us                                                 | 686 us: 1.57x slower                                                   |
| django_template            | 44.9 ms                                                | 71.0 ms: 1.58x slower                                                  |
| unpickle_pure_python       | 300 us                                                 | 476 us: 1.59x slower                                                   |
| sympy_str                  | 385 ms                                                 | 617 ms: 1.60x slower                                                   |
| scimark_lu                 | 152 ms                                                 | 244 ms: 1.60x slower                                                   |
| nbody                      | 119 ms                                                 | 195 ms: 1.64x slower                                                   |
| sqlalchemy_imperative      | 24.7 ms                                                | 41.1 ms: 1.67x slower                                                  |
| logging_format             | 9.59 us                                                | 16.1 us: 1.68x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 3.28 ms: 1.69x slower                                                  |
| richards                   | 60.3 ms                                                | 103 ms: 1.70x slower                                                   |
| raytrace                   | 408 ms                                                 | 702 ms: 1.72x slower                                                   |
| logging_silent             | 139 ns                                                 | 241 ns: 1.73x slower                                                   |
| mako                       | 15.7 ms                                                | 27.7 ms: 1.76x slower                                                  |
| chaos                      | 84.9 ms                                                | 150 ms: 1.76x slower                                                   |
| sqlglot_parse              | 1.79 ms                                                | 3.28 ms: 1.84x slower                                                  |
| scimark_sor                | 167 ms                                                 | 308 ms: 1.85x slower                                                   |
| hexiom                     | 8.27 ms                                                | 15.4 ms: 1.86x slower                                                  |
| go                         | 172 ms                                                 | 325 ms: 1.89x slower                                                   |
| sqlglot_transpile          | 2.34 ms                                                | 4.42 ms: 1.89x slower                                                  |
| sympy_sum                  | 222 ms                                                 | 452 ms: 2.04x slower                                                   |
| sympy_expand               | 582 ms                                                 | 1.23 sec: 2.11x slower                                                 |
| deltablue                  | 4.27 ms                                                | 11.1 ms: 2.61x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 105 ms: 5.07x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.28x slower                                                           |

Benchmark hidden because not significant (5): sqlite_synth, json_loads, asyncio_websockets, gc_traversal, bench_thread_pool
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241203-3.14.0a2+-bfb0788-NOGIL/bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.204x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.20x
- 95% likely to have a slowdown of 1.18x
- 99% likely to have a slowdown of 1.15x

# Memory
- memory change: 1.34x