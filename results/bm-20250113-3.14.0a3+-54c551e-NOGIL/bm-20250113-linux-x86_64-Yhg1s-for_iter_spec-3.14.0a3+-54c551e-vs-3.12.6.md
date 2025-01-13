# Results vs. 3.12.6

- fork: Yhg1s
- ref: for_iter_spec
- machine: linux-x86_64
- commit hash: 54c551e
- commit date: 2025-01-13
- overall geometric mean: 1.165x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-54c551e |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 648 ms: 1.42x slower                                           |
| docutils       | 4.00 sec                                               | 4.96 sec: 1.24x slower                                         |
| html5lib       | 88.9 ms                                                | 130 ms: 1.46x slower                                           |
| Geometric mean | (ref)                                                  | 1.37x slower                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-54c551e |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 987 ms: 1.96x faster                                           |
| async_tree_io              | 1.85 sec                                               | 1.07 sec: 1.73x faster                                         |
| async_tree_memoization_tg  | 930 ms                                                 | 564 ms: 1.65x faster                                           |
| async_tree_none_tg         | 704 ms                                                 | 428 ms: 1.64x faster                                           |
| async_tree_memoization     | 977 ms                                                 | 651 ms: 1.50x faster                                           |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 741 ms: 1.49x faster                                           |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 819 ms: 1.32x faster                                           |
| async_tree_none            | 741 ms                                                 | 610 ms: 1.22x faster                                           |
| coroutines                 | 29.5 ms                                                | 33.8 ms: 1.14x slower                                          |
| async_generators           | 589 ms                                                 | 715 ms: 1.21x slower                                           |
| Geometric mean             | (ref)                                                  | 1.34x faster                                                   |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-54c551e |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| pidigits       | 250 ms                                                 | 238 ms: 1.05x faster                                           |
| float          | 123 ms                                                 | 144 ms: 1.17x slower                                           |
| nbody          | 119 ms                                                 | 168 ms: 1.41x slower                                           |
| Geometric mean | (ref)                                                  | 1.16x slower                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-54c551e |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.83 ms: 1.06x faster                                          |
| regex_dna      | 278 ms                                                 | 335 ms: 1.21x slower                                           |
| regex_compile  | 187 ms                                                 | 231 ms: 1.24x slower                                           |
| regex_v8       | 32.5 ms                                                | 40.7 ms: 1.25x slower                                          |
| Geometric mean | (ref)                                                  | 1.15x slower                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-54c551e |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| xml_etree_iterparse  | 169 ms                                                 | 141 ms: 1.20x faster                                           |
| xml_etree_parse      | 241 ms                                                 | 223 ms: 1.08x faster                                           |
| json_loads           | 37.9 us                                                | 40.1 us: 1.06x slower                                          |
| tomli_loads          | 2.88 sec                                               | 3.09 sec: 1.07x slower                                         |
| xml_etree_generate   | 127 ms                                                 | 150 ms: 1.18x slower                                           |
| json_dumps           | 14.3 ms                                                | 18.9 ms: 1.32x slower                                          |
| xml_etree_process    | 83.7 ms                                                | 116 ms: 1.39x slower                                           |
| pickle_pure_python   | 436 us                                                 | 611 us: 1.40x slower                                           |
| unpickle_pure_python | 300 us                                                 | 436 us: 1.45x slower                                           |
| Geometric mean       | (ref)                                                  | 1.16x slower                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-54c551e |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 22.3 ms: 1.27x slower                                          |
| python_startup         | 23.7 ms                                                | 34.5 ms: 1.46x slower                                          |
| Geometric mean         | (ref)                                                  | 1.36x slower                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-54c551e |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 85.3 ms: 1.26x slower                                          |
| genshi_text     | 30.2 ms                                                | 42.8 ms: 1.41x slower                                          |
| django_template | 44.9 ms                                                | 63.8 ms: 1.42x slower                                          |
| mako            | 15.7 ms                                                | 29.2 ms: 1.85x slower                                          |
| Geometric mean  | (ref)                                                  | 1.47x slower                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-54c551e |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 987 ms: 1.96x faster                                           |
| async_tree_io              | 1.85 sec                                               | 1.07 sec: 1.73x faster                                         |
| async_tree_memoization_tg  | 930 ms                                                 | 564 ms: 1.65x faster                                           |
| async_tree_none_tg         | 704 ms                                                 | 428 ms: 1.64x faster                                           |
| async_tree_memoization     | 977 ms                                                 | 651 ms: 1.50x faster                                           |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 741 ms: 1.49x faster                                           |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 819 ms: 1.32x faster                                           |
| async_tree_none            | 741 ms                                                 | 610 ms: 1.22x faster                                           |
| xml_etree_iterparse        | 169 ms                                                 | 141 ms: 1.20x faster                                           |
| xml_etree_parse            | 241 ms                                                 | 223 ms: 1.08x faster                                           |
| deepcopy                   | 468 us                                                 | 439 us: 1.07x faster                                           |
| regex_effbot               | 5.13 ms                                                | 4.83 ms: 1.06x faster                                          |
| pidigits                   | 250 ms                                                 | 238 ms: 1.05x faster                                           |
| json_loads                 | 37.9 us                                                | 40.1 us: 1.06x slower                                          |
| deepcopy_reduce            | 4.04 us                                                | 4.27 us: 1.06x slower                                          |
| tomli_loads                | 2.88 sec                                               | 3.09 sec: 1.07x slower                                         |
| sqlglot_optimize           | 76.0 ms                                                | 82.5 ms: 1.09x slower                                          |
| deepcopy_memo              | 52.4 us                                                | 58.0 us: 1.11x slower                                          |
| scimark_fft                | 500 ms                                                 | 555 ms: 1.11x slower                                           |
| sympy_sum                  | 222 ms                                                 | 250 ms: 1.13x slower                                           |
| json                       | 6.85 ms                                                | 7.76 ms: 1.13x slower                                          |
| coroutines                 | 29.5 ms                                                | 33.8 ms: 1.14x slower                                          |
| float                      | 123 ms                                                 | 144 ms: 1.17x slower                                           |
| sympy_str                  | 385 ms                                                 | 450 ms: 1.17x slower                                           |
| pylint                     | 465 ms                                                 | 545 ms: 1.17x slower                                           |
| mdp                        | 3.97 sec                                               | 4.67 sec: 1.18x slower                                         |
| xml_etree_generate         | 127 ms                                                 | 150 ms: 1.18x slower                                           |
| bpe_tokeniser              | 6.59 sec                                               | 7.75 sec: 1.18x slower                                         |
| spectral_norm              | 156 ms                                                 | 184 ms: 1.18x slower                                           |
| meteor_contest             | 146 ms                                                 | 176 ms: 1.20x slower                                           |
| regex_dna                  | 278 ms                                                 | 335 ms: 1.21x slower                                           |
| async_generators           | 589 ms                                                 | 715 ms: 1.21x slower                                           |
| nqueens                    | 117 ms                                                 | 143 ms: 1.22x slower                                           |
| typing_runtime_protocols   | 224 us                                                 | 274 us: 1.22x slower                                           |
| sqlalchemy_declarative     | 218 ms                                                 | 268 ms: 1.23x slower                                           |
| bench_thread_pool          | 3.48 ms                                                | 4.30 ms: 1.24x slower                                          |
| regex_compile              | 187 ms                                                 | 231 ms: 1.24x slower                                           |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 8.31 ms: 1.24x slower                                          |
| docutils                   | 4.00 sec                                               | 4.96 sec: 1.24x slower                                         |
| regex_v8                   | 32.5 ms                                                | 40.7 ms: 1.25x slower                                          |
| pyflate                    | 727 ms                                                 | 913 ms: 1.26x slower                                           |
| genshi_xml                 | 67.6 ms                                                | 85.3 ms: 1.26x slower                                          |
| python_startup_no_site     | 17.6 ms                                                | 22.3 ms: 1.27x slower                                          |
| fannkuch                   | 540 ms                                                 | 685 ms: 1.27x slower                                           |
| sympy_integrate            | 29.8 ms                                                | 39.0 ms: 1.31x slower                                          |
| pprint_safe_repr           | 967 ms                                                 | 1.27 sec: 1.31x slower                                         |
| json_dumps                 | 14.3 ms                                                | 18.9 ms: 1.32x slower                                          |
| dulwich_log                | 100 ms                                                 | 133 ms: 1.33x slower                                           |
| gc_traversal               | 5.86 ms                                                | 7.83 ms: 1.34x slower                                          |
| pprint_pformat             | 1.98 sec                                               | 2.67 sec: 1.35x slower                                         |
| scimark_monte_carlo        | 96.4 ms                                                | 130 ms: 1.35x slower                                           |
| richards_super             | 72.8 ms                                                | 98.3 ms: 1.35x slower                                          |
| comprehensions             | 27.1 us                                                | 36.7 us: 1.35x slower                                          |
| sympy_expand               | 582 ms                                                 | 793 ms: 1.36x slower                                           |
| scimark_lu                 | 152 ms                                                 | 209 ms: 1.37x slower                                           |
| xml_etree_process          | 83.7 ms                                                | 116 ms: 1.39x slower                                           |
| generators                 | 41.1 ms                                                | 57.3 ms: 1.39x slower                                          |
| pickle_pure_python         | 436 us                                                 | 611 us: 1.40x slower                                           |
| logging_simple             | 9.45 us                                                | 13.3 us: 1.40x slower                                          |
| crypto_pyaes               | 107 ms                                                 | 151 ms: 1.41x slower                                           |
| nbody                      | 119 ms                                                 | 168 ms: 1.41x slower                                           |
| genshi_text                | 30.2 ms                                                | 42.8 ms: 1.41x slower                                          |
| django_template            | 44.9 ms                                                | 63.8 ms: 1.42x slower                                          |
| 2to3                       | 456 ms                                                 | 648 ms: 1.42x slower                                           |
| telco                      | 9.59 ms                                                | 13.7 ms: 1.43x slower                                          |
| thrift                     | 1.06 ms                                                | 1.53 ms: 1.44x slower                                          |
| logging_format             | 9.59 us                                                | 13.9 us: 1.45x slower                                          |
| unpickle_pure_python       | 300 us                                                 | 436 us: 1.45x slower                                           |
| python_startup             | 23.7 ms                                                | 34.5 ms: 1.46x slower                                          |
| html5lib                   | 88.9 ms                                                | 130 ms: 1.46x slower                                           |
| richards                   | 60.3 ms                                                | 90.6 ms: 1.50x slower                                          |
| coverage                   | 95.4 ms                                                | 143 ms: 1.50x slower                                           |
| chaos                      | 84.9 ms                                                | 128 ms: 1.51x slower                                           |
| scimark_sor                | 167 ms                                                 | 253 ms: 1.52x slower                                           |
| sqlglot_transpile          | 2.34 ms                                                | 3.58 ms: 1.53x slower                                          |
| raytrace                   | 408 ms                                                 | 633 ms: 1.55x slower                                           |
| sqlalchemy_imperative      | 24.7 ms                                                | 42.0 ms: 1.70x slower                                          |
| hexiom                     | 8.27 ms                                                | 14.2 ms: 1.71x slower                                          |
| go                         | 172 ms                                                 | 296 ms: 1.72x slower                                           |
| logging_silent             | 139 ns                                                 | 253 ns: 1.82x slower                                           |
| mako                       | 15.7 ms                                                | 29.2 ms: 1.85x slower                                          |
| create_gc_cycles           | 1.94 ms                                                | 3.73 ms: 1.93x slower                                          |
| sqlglot_parse              | 1.79 ms                                                | 3.48 ms: 1.95x slower                                          |
| deltablue                  | 4.27 ms                                                | 10.8 ms: 2.53x slower                                          |
| bench_mp_pool              | 20.7 ms                                                | 102 ms: 4.94x slower                                           |
| Geometric mean             | (ref)                                                  | 1.23x slower                                                   |

Benchmark hidden because not significant (5): pycparser, asyncio_websockets, sqlite_synth, sqlglot_normalize, pathlib
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250113-3.14.0a3+-54c551e-NOGIL/bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-54c551e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.165x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.17x
- 95% likely to have a slowdown of 1.16x
- 99% likely to have a slowdown of 1.14x

# Memory
- memory change: 1.34x