# Results vs. 3.12.6

- fork: mpage
- ref: reapply_gc_changes
- machine: linux-x86_64
- commit hash: 4049072
- commit date: 2024-12-03
- overall geometric mean: 1.255x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.21x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-mpage-reapply_gc_changes-3.14.0a2+-4049072 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 375 ms: 1.42x slower                                                |
| docutils       | 2.64 sec                                               | 3.20 sec: 1.21x slower                                              |
| html5lib       | 63.6 ms                                                | 100 ms: 1.58x slower                                                |
| Geometric mean | (ref)                                                  | 1.40x slower                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-mpage-reapply_gc_changes-3.14.0a2+-4049072 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 855 ms: 1.30x faster                                                |
| async_tree_none_tg         | 446 ms                                                 | 363 ms: 1.23x faster                                                |
| async_tree_io              | 1.08 sec                                               | 892 ms: 1.21x faster                                                |
| async_tree_memoization_tg  | 560 ms                                                 | 461 ms: 1.21x faster                                                |
| async_tree_none            | 464 ms                                                 | 397 ms: 1.17x faster                                                |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 629 ms: 1.15x faster                                                |
| async_tree_memoization     | 555 ms                                                 | 488 ms: 1.14x faster                                                |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 659 ms: 1.09x faster                                                |
| coroutines                 | 23.9 ms                                                | 27.3 ms: 1.14x slower                                               |
| async_generators           | 384 ms                                                 | 469 ms: 1.22x slower                                                |
| Geometric mean             | (ref)                                                  | 1.10x faster                                                        |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-mpage-reapply_gc_changes-3.14.0a2+-4049072 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 182 ms: 1.01x faster                                                |
| nbody          | 89.3 ms                                                | 128 ms: 1.43x slower                                                |
| float          | 80.8 ms                                                | 143 ms: 1.77x slower                                                |
| Geometric mean | (ref)                                                  | 1.36x slower                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-mpage-reapply_gc_changes-3.14.0a2+-4049072 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.89 ms: 1.10x faster                                               |
| regex_dna      | 168 ms                                                 | 182 ms: 1.09x slower                                                |
| regex_v8       | 20.6 ms                                                | 24.0 ms: 1.17x slower                                               |
| regex_compile  | 142 ms                                                 | 194 ms: 1.36x slower                                                |
| Geometric mean | (ref)                                                  | 1.12x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-mpage-reapply_gc_changes-3.14.0a2+-4049072 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.06x faster                                                |
| xml_etree_iterparse  | 96.7 ms                                                | 95.0 ms: 1.02x faster                                               |
| json_loads           | 26.5 us                                                | 28.0 us: 1.06x slower                                               |
| xml_etree_generate   | 85.2 ms                                                | 104 ms: 1.22x slower                                                |
| tomli_loads          | 2.11 sec                                               | 2.75 sec: 1.31x slower                                              |
| xml_etree_process    | 59.0 ms                                                | 82.6 ms: 1.40x slower                                               |
| json_dumps           | 10.4 ms                                                | 14.6 ms: 1.41x slower                                               |
| unpickle_pure_python | 221 us                                                 | 373 us: 1.69x slower                                                |
| pickle_pure_python   | 308 us                                                 | 560 us: 1.82x slower                                                |
| Geometric mean       | (ref)                                                  | 1.28x slower                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-mpage-reapply_gc_changes-3.14.0a2+-4049072 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.3 ms: 1.43x slower                                               |
| python_startup         | 9.93 ms                                                | 17.5 ms: 1.76x slower                                               |
| Geometric mean         | (ref)                                                  | 1.59x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-mpage-reapply_gc_changes-3.14.0a2+-4049072 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 66.2 ms: 1.32x slower                                               |
| genshi_text     | 22.8 ms                                                | 33.3 ms: 1.46x slower                                               |
| django_template | 34.7 ms                                                | 55.7 ms: 1.61x slower                                               |
| mako            | 11.0 ms                                                | 19.6 ms: 1.78x slower                                               |
| Geometric mean  | (ref)                                                  | 1.53x slower                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-mpage-reapply_gc_changes-3.14.0a2+-4049072 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 855 ms: 1.30x faster                                                |
| async_tree_none_tg         | 446 ms                                                 | 363 ms: 1.23x faster                                                |
| async_tree_io              | 1.08 sec                                               | 892 ms: 1.21x faster                                                |
| async_tree_memoization_tg  | 560 ms                                                 | 461 ms: 1.21x faster                                                |
| async_tree_none            | 464 ms                                                 | 397 ms: 1.17x faster                                                |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 629 ms: 1.15x faster                                                |
| async_tree_memoization     | 555 ms                                                 | 488 ms: 1.14x faster                                                |
| regex_effbot               | 3.17 ms                                                | 2.89 ms: 1.10x faster                                               |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 659 ms: 1.09x faster                                                |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.06x faster                                                |
| pathlib                    | 21.5 ms                                                | 20.6 ms: 1.04x faster                                               |
| xml_etree_iterparse        | 96.7 ms                                                | 95.0 ms: 1.02x faster                                               |
| pidigits                   | 184 ms                                                 | 182 ms: 1.01x faster                                                |
| deepcopy                   | 352 us                                                 | 358 us: 1.02x slower                                                |
| gc_traversal               | 3.46 ms                                                | 3.52 ms: 1.02x slower                                               |
| sqlite_synth               | 2.20 us                                                | 2.32 us: 1.05x slower                                               |
| json_loads                 | 26.5 us                                                | 28.0 us: 1.06x slower                                               |
| regex_dna                  | 168 ms                                                 | 182 ms: 1.09x slower                                                |
| deepcopy_memo              | 40.3 us                                                | 45.2 us: 1.12x slower                                               |
| coroutines                 | 23.9 ms                                                | 27.3 ms: 1.14x slower                                               |
| bpe_tokeniser              | 4.74 sec                                               | 5.43 sec: 1.15x slower                                              |
| regex_v8                   | 20.6 ms                                                | 24.0 ms: 1.17x slower                                               |
| spectral_norm              | 110 ms                                                 | 130 ms: 1.18x slower                                                |
| scimark_fft                | 342 ms                                                 | 403 ms: 1.18x slower                                                |
| generators                 | 32.2 ms                                                | 38.5 ms: 1.19x slower                                               |
| crypto_pyaes               | 76.6 ms                                                | 92.7 ms: 1.21x slower                                               |
| deepcopy_reduce            | 3.08 us                                                | 3.73 us: 1.21x slower                                               |
| docutils                   | 2.64 sec                                               | 3.20 sec: 1.21x slower                                              |
| xml_etree_generate         | 85.2 ms                                                | 104 ms: 1.22x slower                                                |
| async_generators           | 384 ms                                                 | 469 ms: 1.22x slower                                                |
| mdp                        | 2.42 sec                                               | 2.96 sec: 1.22x slower                                              |
| pylint                     | 319 ms                                                 | 392 ms: 1.23x slower                                                |
| dulwich_log                | 78.9 ms                                                | 98.5 ms: 1.25x slower                                               |
| nqueens                    | 80.1 ms                                                | 104 ms: 1.30x slower                                                |
| meteor_contest             | 104 ms                                                 | 135 ms: 1.30x slower                                                |
| tomli_loads                | 2.11 sec                                               | 2.75 sec: 1.31x slower                                              |
| typing_runtime_protocols   | 163 us                                                 | 214 us: 1.31x slower                                                |
| genshi_xml                 | 50.2 ms                                                | 66.2 ms: 1.32x slower                                               |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.94 ms: 1.35x slower                                               |
| regex_compile              | 142 ms                                                 | 194 ms: 1.36x slower                                                |
| fannkuch                   | 372 ms                                                 | 511 ms: 1.37x slower                                                |
| telco                      | 6.53 ms                                                | 8.98 ms: 1.38x slower                                               |
| sqlalchemy_imperative      | 21.8 ms                                                | 30.2 ms: 1.38x slower                                               |
| pycparser                  | 1.17 sec                                               | 1.63 sec: 1.39x slower                                              |
| xml_etree_process          | 59.0 ms                                                | 82.6 ms: 1.40x slower                                               |
| json_dumps                 | 10.4 ms                                                | 14.6 ms: 1.41x slower                                               |
| coverage                   | 71.4 ms                                                | 101 ms: 1.41x slower                                                |
| sqlglot_optimize           | 53.3 ms                                                | 75.4 ms: 1.42x slower                                               |
| sqlglot_normalize          | 107 ms                                                 | 151 ms: 1.42x slower                                                |
| 2to3                       | 264 ms                                                 | 375 ms: 1.42x slower                                                |
| nbody                      | 89.3 ms                                                | 128 ms: 1.43x slower                                                |
| python_startup_no_site     | 7.16 ms                                                | 10.3 ms: 1.43x slower                                               |
| pprint_safe_repr           | 743 ms                                                 | 1.08 sec: 1.45x slower                                              |
| sqlalchemy_declarative     | 143 ms                                                 | 207 ms: 1.45x slower                                                |
| genshi_text                | 22.8 ms                                                | 33.3 ms: 1.46x slower                                               |
| comprehensions             | 19.8 us                                                | 29.0 us: 1.46x slower                                               |
| pprint_pformat             | 1.52 sec                                               | 2.22 sec: 1.46x slower                                              |
| sympy_integrate            | 20.5 ms                                                | 30.6 ms: 1.49x slower                                               |
| thrift                     | 791 us                                                 | 1.20 ms: 1.52x slower                                               |
| html5lib                   | 63.6 ms                                                | 100 ms: 1.58x slower                                                |
| django_template            | 34.7 ms                                                | 55.7 ms: 1.61x slower                                               |
| pyflate                    | 448 ms                                                 | 728 ms: 1.63x slower                                                |
| logging_simple             | 6.63 us                                                | 11.1 us: 1.68x slower                                               |
| sympy_str                  | 292 ms                                                 | 492 ms: 1.69x slower                                                |
| logging_format             | 7.35 us                                                | 12.4 us: 1.69x slower                                               |
| unpickle_pure_python       | 221 us                                                 | 373 us: 1.69x slower                                                |
| create_gc_cycles           | 1.09 ms                                                | 1.86 ms: 1.71x slower                                               |
| scimark_lu                 | 114 ms                                                 | 195 ms: 1.71x slower                                                |
| hexiom                     | 6.17 ms                                                | 10.6 ms: 1.72x slower                                               |
| chaos                      | 62.8 ms                                                | 110 ms: 1.75x slower                                                |
| python_startup             | 9.93 ms                                                | 17.5 ms: 1.76x slower                                               |
| float                      | 80.8 ms                                                | 143 ms: 1.77x slower                                                |
| scimark_monte_carlo        | 68.4 ms                                                | 121 ms: 1.77x slower                                                |
| mako                       | 11.0 ms                                                | 19.6 ms: 1.78x slower                                               |
| richards                   | 45.9 ms                                                | 82.1 ms: 1.79x slower                                               |
| logging_silent             | 109 ns                                                 | 196 ns: 1.80x slower                                                |
| pickle_pure_python         | 308 us                                                 | 560 us: 1.82x slower                                                |
| sqlglot_transpile          | 1.67 ms                                                | 3.06 ms: 1.83x slower                                               |
| scimark_sor                | 130 ms                                                 | 239 ms: 1.85x slower                                                |
| richards_super             | 51.9 ms                                                | 99.7 ms: 1.92x slower                                               |
| sqlglot_parse              | 1.36 ms                                                | 2.65 ms: 1.95x slower                                               |
| raytrace                   | 299 ms                                                 | 593 ms: 1.98x slower                                                |
| go                         | 139 ms                                                 | 276 ms: 1.98x slower                                                |
| sympy_expand               | 468 ms                                                 | 985 ms: 2.11x slower                                                |
| sympy_sum                  | 166 ms                                                 | 358 ms: 2.15x slower                                                |
| deltablue                  | 3.45 ms                                                | 8.60 ms: 2.50x slower                                               |
| bench_thread_pool          | 941 us                                                 | 3.39 ms: 3.60x slower                                               |
| bench_mp_pool              | 10.8 ms                                                | 110 ms: 10.15x slower                                               |
| Geometric mean             | (ref)                                                  | 1.39x slower                                                        |

Benchmark hidden because not significant (2): asyncio_websockets, json
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241203-3.14.0a2+-4049072-NOGIL/bm-20241203-vultr-x86_64-mpage-reapply_gc_changes-3.14.0a2+-4049072.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.255x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.26x
- 95% likely to have a slowdown of 1.23x
- 99% likely to have a slowdown of 1.21x

# Memory
- memory change: 1.33x