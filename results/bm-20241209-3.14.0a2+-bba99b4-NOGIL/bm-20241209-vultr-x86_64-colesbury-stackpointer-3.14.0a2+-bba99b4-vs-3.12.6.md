# Results vs. 3.12.6

- fork: colesbury
- ref: stackpointer
- machine: linux-x86_64
- commit hash: bba99b4
- commit date: 2024-12-09
- overall geometric mean: 1.234x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.19x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2+-bba99b4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 372 ms: 1.41x slower                                              |
| docutils       | 2.64 sec                                               | 3.11 sec: 1.18x slower                                            |
| html5lib       | 63.6 ms                                                | 98.0 ms: 1.54x slower                                             |
| Geometric mean | (ref)                                                  | 1.37x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2+-bba99b4 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 838 ms: 1.32x faster                                              |
| async_tree_io              | 1.08 sec                                               | 864 ms: 1.25x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 366 ms: 1.22x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 460 ms: 1.22x faster                                              |
| async_tree_none            | 464 ms                                                 | 399 ms: 1.16x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 627 ms: 1.15x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 482 ms: 1.15x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 654 ms: 1.09x faster                                              |
| asyncio_websockets         | 517 ms                                                 | 521 ms: 1.01x slower                                              |
| coroutines                 | 23.9 ms                                                | 25.1 ms: 1.05x slower                                             |
| async_generators           | 384 ms                                                 | 469 ms: 1.22x slower                                              |
| Geometric mean             | (ref)                                                  | 1.11x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2+-bba99b4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 184 ms: 1.00x faster                                              |
| nbody          | 89.3 ms                                                | 134 ms: 1.50x slower                                              |
| float          | 80.8 ms                                                | 142 ms: 1.75x slower                                              |
| Geometric mean | (ref)                                                  | 1.38x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2+-bba99b4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.73 ms: 1.16x faster                                             |
| regex_dna      | 168 ms                                                 | 176 ms: 1.05x slower                                              |
| regex_v8       | 20.6 ms                                                | 24.1 ms: 1.17x slower                                             |
| regex_compile  | 142 ms                                                 | 185 ms: 1.30x slower                                              |
| Geometric mean | (ref)                                                  | 1.08x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2+-bba99b4 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                              |
| xml_etree_iterparse  | 96.7 ms                                                | 91.5 ms: 1.06x faster                                             |
| json_loads           | 26.5 us                                                | 28.6 us: 1.08x slower                                             |
| xml_etree_generate   | 85.2 ms                                                | 99.5 ms: 1.17x slower                                             |
| tomli_loads          | 2.11 sec                                               | 2.72 sec: 1.29x slower                                            |
| xml_etree_process    | 59.0 ms                                                | 78.8 ms: 1.34x slower                                             |
| json_dumps           | 10.4 ms                                                | 14.3 ms: 1.38x slower                                             |
| unpickle_pure_python | 221 us                                                 | 339 us: 1.54x slower                                              |
| pickle_pure_python   | 308 us                                                 | 520 us: 1.69x slower                                              |
| Geometric mean       | (ref)                                                  | 1.24x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2+-bba99b4 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.2 ms: 1.43x slower                                             |
| python_startup         | 9.93 ms                                                | 17.4 ms: 1.75x slower                                             |
| Geometric mean         | (ref)                                                  | 1.58x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2+-bba99b4 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 66.0 ms: 1.32x slower                                             |
| genshi_text     | 22.8 ms                                                | 32.3 ms: 1.42x slower                                             |
| django_template | 34.7 ms                                                | 51.5 ms: 1.49x slower                                             |
| mako            | 11.0 ms                                                | 18.2 ms: 1.65x slower                                             |
| Geometric mean  | (ref)                                                  | 1.46x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2+-bba99b4 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 838 ms: 1.32x faster                                              |
| async_tree_io              | 1.08 sec                                               | 864 ms: 1.25x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 366 ms: 1.22x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 460 ms: 1.22x faster                                              |
| async_tree_none            | 464 ms                                                 | 399 ms: 1.16x faster                                              |
| regex_effbot               | 3.17 ms                                                | 2.73 ms: 1.16x faster                                             |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 627 ms: 1.15x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 482 ms: 1.15x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 654 ms: 1.09x faster                                              |
| gc_traversal               | 3.46 ms                                                | 3.17 ms: 1.09x faster                                             |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                              |
| xml_etree_iterparse        | 96.7 ms                                                | 91.5 ms: 1.06x faster                                             |
| deepcopy                   | 352 us                                                 | 333 us: 1.06x faster                                              |
| pathlib                    | 21.5 ms                                                | 20.6 ms: 1.04x faster                                             |
| pidigits                   | 184 ms                                                 | 184 ms: 1.00x faster                                              |
| asyncio_websockets         | 517 ms                                                 | 521 ms: 1.01x slower                                              |
| deepcopy_memo              | 40.3 us                                                | 40.6 us: 1.01x slower                                             |
| json                       | 5.02 ms                                                | 5.07 ms: 1.01x slower                                             |
| regex_dna                  | 168 ms                                                 | 176 ms: 1.05x slower                                              |
| coroutines                 | 23.9 ms                                                | 25.1 ms: 1.05x slower                                             |
| sqlite_synth               | 2.20 us                                                | 2.32 us: 1.05x slower                                             |
| bpe_tokeniser              | 4.74 sec                                               | 5.05 sec: 1.07x slower                                            |
| json_loads                 | 26.5 us                                                | 28.6 us: 1.08x slower                                             |
| spectral_norm              | 110 ms                                                 | 123 ms: 1.11x slower                                              |
| mdp                        | 2.42 sec                                               | 2.80 sec: 1.16x slower                                            |
| deepcopy_reduce            | 3.08 us                                                | 3.56 us: 1.16x slower                                             |
| xml_etree_generate         | 85.2 ms                                                | 99.5 ms: 1.17x slower                                             |
| regex_v8                   | 20.6 ms                                                | 24.1 ms: 1.17x slower                                             |
| docutils                   | 2.64 sec                                               | 3.11 sec: 1.18x slower                                            |
| scimark_fft                | 342 ms                                                 | 410 ms: 1.20x slower                                              |
| pylint                     | 319 ms                                                 | 385 ms: 1.21x slower                                              |
| async_generators           | 384 ms                                                 | 469 ms: 1.22x slower                                              |
| crypto_pyaes               | 76.6 ms                                                | 94.3 ms: 1.23x slower                                             |
| generators                 | 32.2 ms                                                | 39.8 ms: 1.23x slower                                             |
| dulwich_log                | 78.9 ms                                                | 97.6 ms: 1.24x slower                                             |
| nqueens                    | 80.1 ms                                                | 99.5 ms: 1.24x slower                                             |
| meteor_contest             | 104 ms                                                 | 131 ms: 1.26x slower                                              |
| typing_runtime_protocols   | 163 us                                                 | 208 us: 1.28x slower                                              |
| tomli_loads                | 2.11 sec                                               | 2.72 sec: 1.29x slower                                            |
| regex_compile              | 142 ms                                                 | 185 ms: 1.30x slower                                              |
| genshi_xml                 | 50.2 ms                                                | 66.0 ms: 1.32x slower                                             |
| sqlglot_optimize           | 53.3 ms                                                | 70.6 ms: 1.33x slower                                             |
| sqlglot_normalize          | 107 ms                                                 | 142 ms: 1.33x slower                                              |
| xml_etree_process          | 59.0 ms                                                | 78.8 ms: 1.34x slower                                             |
| pycparser                  | 1.17 sec                                               | 1.58 sec: 1.35x slower                                            |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.93 ms: 1.35x slower                                             |
| telco                      | 6.53 ms                                                | 8.82 ms: 1.35x slower                                             |
| pprint_safe_repr           | 743 ms                                                 | 1.01 sec: 1.36x slower                                            |
| pprint_pformat             | 1.52 sec                                               | 2.08 sec: 1.37x slower                                            |
| sqlalchemy_imperative      | 21.8 ms                                                | 29.9 ms: 1.37x slower                                             |
| fannkuch                   | 372 ms                                                 | 514 ms: 1.38x slower                                              |
| json_dumps                 | 10.4 ms                                                | 14.3 ms: 1.38x slower                                             |
| comprehensions             | 19.8 us                                                | 27.9 us: 1.41x slower                                             |
| coverage                   | 71.4 ms                                                | 101 ms: 1.41x slower                                              |
| 2to3                       | 264 ms                                                 | 372 ms: 1.41x slower                                              |
| genshi_text                | 22.8 ms                                                | 32.3 ms: 1.42x slower                                             |
| python_startup_no_site     | 7.16 ms                                                | 10.2 ms: 1.43x slower                                             |
| sqlalchemy_declarative     | 143 ms                                                 | 205 ms: 1.44x slower                                              |
| sympy_integrate            | 20.5 ms                                                | 29.7 ms: 1.45x slower                                             |
| thrift                     | 791 us                                                 | 1.16 ms: 1.47x slower                                             |
| django_template            | 34.7 ms                                                | 51.5 ms: 1.49x slower                                             |
| nbody                      | 89.3 ms                                                | 134 ms: 1.50x slower                                              |
| unpickle_pure_python       | 221 us                                                 | 339 us: 1.54x slower                                              |
| html5lib                   | 63.6 ms                                                | 98.0 ms: 1.54x slower                                             |
| pyflate                    | 448 ms                                                 | 693 ms: 1.55x slower                                              |
| scimark_lu                 | 114 ms                                                 | 184 ms: 1.61x slower                                              |
| hexiom                     | 6.17 ms                                                | 10.1 ms: 1.64x slower                                             |
| mako                       | 11.0 ms                                                | 18.2 ms: 1.65x slower                                             |
| sympy_str                  | 292 ms                                                 | 482 ms: 1.65x slower                                              |
| create_gc_cycles           | 1.09 ms                                                | 1.81 ms: 1.66x slower                                             |
| logging_format             | 7.35 us                                                | 12.2 us: 1.66x slower                                             |
| logging_simple             | 6.63 us                                                | 11.0 us: 1.66x slower                                             |
| chaos                      | 62.8 ms                                                | 106 ms: 1.69x slower                                              |
| pickle_pure_python         | 308 us                                                 | 520 us: 1.69x slower                                              |
| logging_silent             | 109 ns                                                 | 187 ns: 1.71x slower                                              |
| richards_super             | 51.9 ms                                                | 89.0 ms: 1.72x slower                                             |
| richards                   | 45.9 ms                                                | 79.0 ms: 1.72x slower                                             |
| python_startup             | 9.93 ms                                                | 17.4 ms: 1.75x slower                                             |
| float                      | 80.8 ms                                                | 142 ms: 1.75x slower                                              |
| scimark_monte_carlo        | 68.4 ms                                                | 121 ms: 1.76x slower                                              |
| sqlglot_transpile          | 1.67 ms                                                | 3.00 ms: 1.79x slower                                             |
| scimark_sor                | 130 ms                                                 | 237 ms: 1.83x slower                                              |
| raytrace                   | 299 ms                                                 | 555 ms: 1.86x slower                                              |
| sqlglot_parse              | 1.36 ms                                                | 2.60 ms: 1.92x slower                                             |
| go                         | 139 ms                                                 | 274 ms: 1.97x slower                                              |
| sympy_expand               | 468 ms                                                 | 963 ms: 2.06x slower                                              |
| sympy_sum                  | 166 ms                                                 | 352 ms: 2.12x slower                                              |
| deltablue                  | 3.45 ms                                                | 8.21 ms: 2.38x slower                                             |
| bench_thread_pool          | 941 us                                                 | 3.44 ms: 3.65x slower                                             |
| bench_mp_pool              | 10.8 ms                                                | 109 ms: 10.09x slower                                             |
| Geometric mean             | (ref)                                                  | 1.35x slower                                                      |
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241209-3.14.0a2+-bba99b4-NOGIL/bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2+-bba99b4.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.234x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.23x
- 95% likely to have a slowdown of 1.22x
- 99% likely to have a slowdown of 1.19x

# Memory
- memory change: 1.33x