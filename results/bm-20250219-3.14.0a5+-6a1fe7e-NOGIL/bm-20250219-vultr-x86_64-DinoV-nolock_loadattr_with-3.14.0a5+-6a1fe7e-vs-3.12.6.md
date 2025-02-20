# Results vs. 3.12.6

- fork: DinoV
- ref: nolock_loadattr_with
- machine: linux-x86_64
- commit hash: 6a1fe7e
- commit date: 2025-02-19
- overall geometric mean: 1.038x slower
- HPT reliability: 99.95%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5+-6a1fe7e |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 300 ms: 1.14x slower                                                  |
| docutils       | 2.64 sec                                               | 2.78 sec: 1.05x slower                                                |
| html5lib       | 63.6 ms                                                | 69.5 ms: 1.09x slower                                                 |
| Geometric mean | (ref)                                                  | 1.09x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5+-6a1fe7e |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 555 ms: 2.00x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 240 ms: 1.86x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 584 ms: 1.86x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 309 ms: 1.81x faster                                                  |
| async_tree_none            | 464 ms                                                 | 278 ms: 1.67x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 339 ms: 1.64x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 488 ms: 1.48x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 521 ms: 1.37x faster                                                  |
| async_generators           | 384 ms                                                 | 370 ms: 1.04x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.1 ms: 1.04x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.48x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5+-6a1fe7e |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 76.1 ms: 1.06x faster                                                 |
| pidigits       | 184 ms                                                 | 196 ms: 1.06x slower                                                  |
| nbody          | 89.3 ms                                                | 132 ms: 1.48x slower                                                  |
| Geometric mean | (ref)                                                  | 1.14x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5+-6a1fe7e |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.88 ms: 1.10x faster                                                 |
| regex_dna      | 168 ms                                                 | 176 ms: 1.05x slower                                                  |
| regex_compile  | 142 ms                                                 | 154 ms: 1.08x slower                                                  |
| regex_v8       | 20.6 ms                                                | 23.6 ms: 1.14x slower                                                 |
| Geometric mean | (ref)                                                  | 1.04x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5+-6a1fe7e |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.9 ms: 1.10x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.33 sec: 1.10x slower                                                |
| unpickle_pure_python | 221 us                                                 | 244 us: 1.11x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 95.4 ms: 1.12x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 355 us: 1.15x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 69.2 ms: 1.17x slower                                                 |
| json_loads           | 26.5 us                                                | 31.5 us: 1.19x slower                                                 |
| json_dumps           | 10.4 ms                                                | 12.8 ms: 1.23x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5+-6a1fe7e |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.59 ms: 1.34x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.5 ms: 1.56x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.45x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5+-6a1fe7e |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.0 ms: 1.18x slower                                                 |
| django_template | 34.7 ms                                                | 41.8 ms: 1.21x slower                                                 |
| genshi_text     | 22.8 ms                                                | 27.7 ms: 1.21x slower                                                 |
| mako            | 11.0 ms                                                | 15.7 ms: 1.43x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.25x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5+-6a1fe7e |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 1.72 ms: 2.01x faster                                                 |
| async_tree_io_tg           | 1.11 sec                                               | 555 ms: 2.00x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 240 ms: 1.86x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 584 ms: 1.86x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 309 ms: 1.81x faster                                                  |
| async_tree_none            | 464 ms                                                 | 278 ms: 1.67x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 339 ms: 1.64x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 488 ms: 1.48x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 521 ms: 1.37x faster                                                  |
| deepcopy                   | 352 us                                                 | 310 us: 1.14x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 87.9 ms: 1.10x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.88 ms: 1.10x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.7 ms: 1.09x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.04 us: 1.08x faster                                                 |
| float                      | 80.8 ms                                                | 76.1 ms: 1.06x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 38.2 us: 1.06x faster                                                 |
| async_generators           | 384 ms                                                 | 370 ms: 1.04x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.1 ms: 1.04x faster                                                 |
| generators                 | 32.2 ms                                                | 31.5 ms: 1.02x faster                                                 |
| go                         | 139 ms                                                 | 137 ms: 1.01x faster                                                  |
| spectral_norm              | 110 ms                                                 | 109 ms: 1.01x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.67 sec: 1.01x faster                                                |
| scimark_sor                | 130 ms                                                 | 131 ms: 1.01x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.19 sec: 1.01x slower                                                |
| deepcopy_reduce            | 3.08 us                                                | 3.20 us: 1.04x slower                                                 |
| dulwich_log                | 78.9 ms                                                | 82.3 ms: 1.04x slower                                                 |
| regex_dna                  | 168 ms                                                 | 176 ms: 1.05x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.78 sec: 1.05x slower                                                |
| json                       | 5.02 ms                                                | 5.34 ms: 1.06x slower                                                 |
| pidigits                   | 184 ms                                                 | 196 ms: 1.06x slower                                                  |
| raytrace                   | 299 ms                                                 | 320 ms: 1.07x slower                                                  |
| logging_simple             | 6.63 us                                                | 7.10 us: 1.07x slower                                                 |
| regex_compile              | 142 ms                                                 | 154 ms: 1.08x slower                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.5 ms: 1.08x slower                                                 |
| logging_format             | 7.35 us                                                | 7.98 us: 1.09x slower                                                 |
| sqlalchemy_declarative     | 143 ms                                                 | 156 ms: 1.09x slower                                                  |
| html5lib                   | 63.6 ms                                                | 69.5 ms: 1.09x slower                                                 |
| pyflate                    | 448 ms                                                 | 491 ms: 1.10x slower                                                  |
| mdp                        | 2.42 sec                                               | 2.67 sec: 1.10x slower                                                |
| tomli_loads                | 2.11 sec                                               | 2.33 sec: 1.10x slower                                                |
| deltablue                  | 3.45 ms                                                | 3.81 ms: 1.11x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 244 us: 1.11x slower                                                  |
| thrift                     | 791 us                                                 | 882 us: 1.11x slower                                                  |
| chaos                      | 62.8 ms                                                | 70.1 ms: 1.12x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 95.4 ms: 1.12x slower                                                 |
| sympy_sum                  | 166 ms                                                 | 186 ms: 1.12x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 832 ms: 1.12x slower                                                  |
| sqlglot_normalize          | 107 ms                                                 | 119 ms: 1.12x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.72 sec: 1.13x slower                                                |
| crypto_pyaes               | 76.6 ms                                                | 86.9 ms: 1.13x slower                                                 |
| sympy_str                  | 292 ms                                                 | 331 ms: 1.14x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.90 ms: 1.14x slower                                                 |
| 2to3                       | 264 ms                                                 | 300 ms: 1.14x slower                                                  |
| scimark_fft                | 342 ms                                                 | 389 ms: 1.14x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 23.6 ms: 1.14x slower                                                 |
| sqlglot_optimize           | 53.3 ms                                                | 61.3 ms: 1.15x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 355 us: 1.15x slower                                                  |
| sympy_expand               | 468 ms                                                 | 542 ms: 1.16x slower                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.58 ms: 1.16x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 23.9 ms: 1.16x slower                                                 |
| hexiom                     | 6.17 ms                                                | 7.23 ms: 1.17x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 69.2 ms: 1.17x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 59.0 ms: 1.18x slower                                                 |
| nqueens                    | 80.1 ms                                                | 94.5 ms: 1.18x slower                                                 |
| richards                   | 45.9 ms                                                | 54.5 ms: 1.19x slower                                                 |
| json_loads                 | 26.5 us                                                | 31.5 us: 1.19x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 82.0 ms: 1.20x slower                                                 |
| django_template            | 34.7 ms                                                | 41.8 ms: 1.21x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 138 ms: 1.21x slower                                                  |
| genshi_text                | 22.8 ms                                                | 27.7 ms: 1.21x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 200 us: 1.22x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 12.8 ms: 1.23x slower                                                 |
| richards_super             | 51.9 ms                                                | 64.0 ms: 1.23x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.36 ms: 1.24x slower                                                 |
| meteor_contest             | 104 ms                                                 | 131 ms: 1.26x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.76 ms: 1.31x slower                                                 |
| fannkuch                   | 372 ms                                                 | 489 ms: 1.31x slower                                                  |
| telco                      | 6.53 ms                                                | 8.70 ms: 1.33x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 9.59 ms: 1.34x slower                                                 |
| coverage                   | 71.4 ms                                                | 98.2 ms: 1.37x slower                                                 |
| mako                       | 11.0 ms                                                | 15.7 ms: 1.43x slower                                                 |
| nbody                      | 89.3 ms                                                | 132 ms: 1.48x slower                                                  |
| python_startup             | 9.93 ms                                                | 15.5 ms: 1.56x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.30 ms: 3.51x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 94.8 ms: 8.78x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.08x slower                                                          |

Benchmark hidden because not significant (4): pylint, logging_silent, asyncio_websockets, comprehensions
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250219-3.14.0a5+-6a1fe7e-NOGIL/bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5+-6a1fe7e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.038x slower

# HPT report

- Reliability score: 99.95% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.36x