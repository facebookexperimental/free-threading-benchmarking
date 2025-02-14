# Results vs. 3.12.6

- fork: DinoV
- ref: set_add_nolock
- machine: linux-x86_64
- commit hash: 247f5bf
- commit date: 2025-02-14
- overall geometric mean: 1.046x slower
- HPT reliability: 99.97%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250214-vultr-x86_64-DinoV-set_add_nolock-3.14.0a5+-247f5bf |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 304 ms: 1.15x slower                                            |
| docutils       | 2.64 sec                                               | 2.80 sec: 1.06x slower                                          |
| html5lib       | 63.6 ms                                                | 71.3 ms: 1.12x slower                                           |
| Geometric mean | (ref)                                                  | 1.11x slower                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250214-vultr-x86_64-DinoV-set_add_nolock-3.14.0a5+-247f5bf |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 580 ms: 1.91x faster                                            |
| async_tree_io              | 1.08 sec                                               | 607 ms: 1.78x faster                                            |
| async_tree_memoization_tg  | 560 ms                                                 | 319 ms: 1.75x faster                                            |
| async_tree_none_tg         | 446 ms                                                 | 258 ms: 1.73x faster                                            |
| async_tree_none            | 464 ms                                                 | 286 ms: 1.62x faster                                            |
| async_tree_memoization     | 555 ms                                                 | 351 ms: 1.58x faster                                            |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 505 ms: 1.43x faster                                            |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 538 ms: 1.33x faster                                            |
| async_generators           | 384 ms                                                 | 372 ms: 1.03x faster                                            |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                           |
| Geometric mean             | (ref)                                                  | 1.44x faster                                                    |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250214-vultr-x86_64-DinoV-set_add_nolock-3.14.0a5+-247f5bf |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------:|
| float          | 80.8 ms                                                | 76.0 ms: 1.06x faster                                           |
| pidigits       | 184 ms                                                 | 213 ms: 1.15x slower                                            |
| nbody          | 89.3 ms                                                | 129 ms: 1.44x slower                                            |
| Geometric mean | (ref)                                                  | 1.16x slower                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250214-vultr-x86_64-DinoV-set_add_nolock-3.14.0a5+-247f5bf |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.86 ms: 1.11x faster                                           |
| regex_compile  | 142 ms                                                 | 152 ms: 1.07x slower                                            |
| regex_dna      | 168 ms                                                 | 182 ms: 1.09x slower                                            |
| regex_v8       | 20.6 ms                                                | 24.1 ms: 1.17x slower                                           |
| Geometric mean | (ref)                                                  | 1.05x slower                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250214-vultr-x86_64-DinoV-set_add_nolock-3.14.0a5+-247f5bf |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.2 ms: 1.10x faster                                           |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.09x faster                                            |
| tomli_loads          | 2.11 sec                                               | 2.34 sec: 1.11x slower                                          |
| xml_etree_generate   | 85.2 ms                                                | 95.8 ms: 1.12x slower                                           |
| unpickle_pure_python | 221 us                                                 | 250 us: 1.13x slower                                            |
| pickle_pure_python   | 308 us                                                 | 363 us: 1.18x slower                                            |
| xml_etree_process    | 59.0 ms                                                | 69.7 ms: 1.18x slower                                           |
| json_loads           | 26.5 us                                                | 31.5 us: 1.19x slower                                           |
| json_dumps           | 10.4 ms                                                | 12.8 ms: 1.24x slower                                           |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250214-vultr-x86_64-DinoV-set_add_nolock-3.14.0a5+-247f5bf |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.61 ms: 1.34x slower                                           |
| python_startup         | 9.93 ms                                                | 15.3 ms: 1.54x slower                                           |
| Geometric mean         | (ref)                                                  | 1.44x slower                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250214-vultr-x86_64-DinoV-set_add_nolock-3.14.0a5+-247f5bf |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.2 ms: 1.18x slower                                           |
| django_template | 34.7 ms                                                | 42.2 ms: 1.22x slower                                           |
| genshi_text     | 22.8 ms                                                | 27.9 ms: 1.22x slower                                           |
| mako            | 11.0 ms                                                | 15.6 ms: 1.42x slower                                           |
| Geometric mean  | (ref)                                                  | 1.26x slower                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250214-vultr-x86_64-DinoV-set_add_nolock-3.14.0a5+-247f5bf |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 1.73 ms: 2.00x faster                                           |
| async_tree_io_tg           | 1.11 sec                                               | 580 ms: 1.91x faster                                            |
| async_tree_io              | 1.08 sec                                               | 607 ms: 1.78x faster                                            |
| async_tree_memoization_tg  | 560 ms                                                 | 319 ms: 1.75x faster                                            |
| async_tree_none_tg         | 446 ms                                                 | 258 ms: 1.73x faster                                            |
| async_tree_none            | 464 ms                                                 | 286 ms: 1.62x faster                                            |
| async_tree_memoization     | 555 ms                                                 | 351 ms: 1.58x faster                                            |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 505 ms: 1.43x faster                                            |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 538 ms: 1.33x faster                                            |
| pathlib                    | 21.5 ms                                                | 19.2 ms: 1.12x faster                                           |
| regex_effbot               | 3.17 ms                                                | 2.86 ms: 1.11x faster                                           |
| deepcopy                   | 352 us                                                 | 320 us: 1.10x faster                                            |
| xml_etree_iterparse        | 96.7 ms                                                | 88.2 ms: 1.10x faster                                           |
| sqlite_synth               | 2.20 us                                                | 2.02 us: 1.09x faster                                           |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.09x faster                                            |
| float                      | 80.8 ms                                                | 76.0 ms: 1.06x faster                                           |
| deepcopy_memo              | 40.3 us                                                | 37.9 us: 1.06x faster                                           |
| spectral_norm              | 110 ms                                                 | 106 ms: 1.04x faster                                            |
| async_generators           | 384 ms                                                 | 372 ms: 1.03x faster                                            |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                           |
| generators                 | 32.2 ms                                                | 31.8 ms: 1.01x faster                                           |
| bpe_tokeniser              | 4.74 sec                                               | 4.68 sec: 1.01x faster                                          |
| comprehensions             | 19.8 us                                                | 19.7 us: 1.01x faster                                           |
| scimark_sor                | 130 ms                                                 | 131 ms: 1.01x slower                                            |
| pycparser                  | 1.17 sec                                               | 1.19 sec: 1.02x slower                                          |
| logging_silent             | 109 ns                                                 | 111 ns: 1.02x slower                                            |
| dulwich_log                | 78.9 ms                                                | 82.8 ms: 1.05x slower                                           |
| deepcopy_reduce            | 3.08 us                                                | 3.25 us: 1.06x slower                                           |
| docutils                   | 2.64 sec                                               | 2.80 sec: 1.06x slower                                          |
| regex_compile              | 142 ms                                                 | 152 ms: 1.07x slower                                            |
| json                       | 5.02 ms                                                | 5.41 ms: 1.08x slower                                           |
| raytrace                   | 299 ms                                                 | 325 ms: 1.09x slower                                            |
| regex_dna                  | 168 ms                                                 | 182 ms: 1.09x slower                                            |
| pyflate                    | 448 ms                                                 | 489 ms: 1.09x slower                                            |
| logging_simple             | 6.63 us                                                | 7.27 us: 1.10x slower                                           |
| pprint_safe_repr           | 743 ms                                                 | 817 ms: 1.10x slower                                            |
| chaos                      | 62.8 ms                                                | 69.2 ms: 1.10x slower                                           |
| sqlalchemy_declarative     | 143 ms                                                 | 158 ms: 1.10x slower                                            |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.1 ms: 1.10x slower                                           |
| tomli_loads                | 2.11 sec                                               | 2.34 sec: 1.11x slower                                          |
| sympy_sum                  | 166 ms                                                 | 185 ms: 1.11x slower                                            |
| pprint_pformat             | 1.52 sec                                               | 1.70 sec: 1.12x slower                                          |
| html5lib                   | 63.6 ms                                                | 71.3 ms: 1.12x slower                                           |
| logging_format             | 7.35 us                                                | 8.24 us: 1.12x slower                                           |
| deltablue                  | 3.45 ms                                                | 3.87 ms: 1.12x slower                                           |
| xml_etree_generate         | 85.2 ms                                                | 95.8 ms: 1.12x slower                                           |
| scimark_fft                | 342 ms                                                 | 385 ms: 1.13x slower                                            |
| unpickle_pure_python       | 221 us                                                 | 250 us: 1.13x slower                                            |
| sqlglot_normalize          | 107 ms                                                 | 121 ms: 1.13x slower                                            |
| thrift                     | 791 us                                                 | 903 us: 1.14x slower                                            |
| sympy_str                  | 292 ms                                                 | 333 ms: 1.14x slower                                            |
| mdp                        | 2.42 sec                                               | 2.77 sec: 1.14x slower                                          |
| sqlglot_transpile          | 1.67 ms                                                | 1.92 ms: 1.15x slower                                           |
| sqlglot_optimize           | 53.3 ms                                                | 61.3 ms: 1.15x slower                                           |
| crypto_pyaes               | 76.6 ms                                                | 88.2 ms: 1.15x slower                                           |
| 2to3                       | 264 ms                                                 | 304 ms: 1.15x slower                                            |
| pidigits                   | 184 ms                                                 | 213 ms: 1.15x slower                                            |
| sympy_expand               | 468 ms                                                 | 544 ms: 1.16x slower                                            |
| regex_v8                   | 20.6 ms                                                | 24.1 ms: 1.17x slower                                           |
| sympy_integrate            | 20.5 ms                                                | 24.0 ms: 1.17x slower                                           |
| sqlglot_parse              | 1.36 ms                                                | 1.59 ms: 1.17x slower                                           |
| genshi_xml                 | 50.2 ms                                                | 59.2 ms: 1.18x slower                                           |
| pickle_pure_python         | 308 us                                                 | 363 us: 1.18x slower                                            |
| xml_etree_process          | 59.0 ms                                                | 69.7 ms: 1.18x slower                                           |
| json_loads                 | 26.5 us                                                | 31.5 us: 1.19x slower                                           |
| scimark_lu                 | 114 ms                                                 | 136 ms: 1.19x slower                                            |
| hexiom                     | 6.17 ms                                                | 7.37 ms: 1.19x slower                                           |
| nqueens                    | 80.1 ms                                                | 95.9 ms: 1.20x slower                                           |
| typing_runtime_protocols   | 163 us                                                 | 198 us: 1.22x slower                                            |
| scimark_monte_carlo        | 68.4 ms                                                | 83.2 ms: 1.22x slower                                           |
| django_template            | 34.7 ms                                                | 42.2 ms: 1.22x slower                                           |
| richards                   | 45.9 ms                                                | 56.1 ms: 1.22x slower                                           |
| genshi_text                | 22.8 ms                                                | 27.9 ms: 1.22x slower                                           |
| json_dumps                 | 10.4 ms                                                | 12.8 ms: 1.24x slower                                           |
| meteor_contest             | 104 ms                                                 | 129 ms: 1.25x slower                                            |
| richards_super             | 51.9 ms                                                | 65.0 ms: 1.25x slower                                           |
| create_gc_cycles           | 1.09 ms                                                | 1.38 ms: 1.26x slower                                           |
| telco                      | 6.53 ms                                                | 8.48 ms: 1.30x slower                                           |
| fannkuch                   | 372 ms                                                 | 485 ms: 1.30x slower                                            |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.73 ms: 1.31x slower                                           |
| coverage                   | 71.4 ms                                                | 95.3 ms: 1.33x slower                                           |
| python_startup_no_site     | 7.16 ms                                                | 9.61 ms: 1.34x slower                                           |
| mako                       | 11.0 ms                                                | 15.6 ms: 1.42x slower                                           |
| nbody                      | 89.3 ms                                                | 129 ms: 1.44x slower                                            |
| python_startup             | 9.93 ms                                                | 15.3 ms: 1.54x slower                                           |
| bench_thread_pool          | 941 us                                                 | 3.33 ms: 3.54x slower                                           |
| bench_mp_pool              | 10.8 ms                                                | 94.7 ms: 8.77x slower                                           |
| Geometric mean             | (ref)                                                  | 1.09x slower                                                    |

Benchmark hidden because not significant (3): pylint, asyncio_websockets, go
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250214-3.14.0a5+-247f5bf-NOGIL/bm-20250214-vultr-x86_64-DinoV-set_add_nolock-3.14.0a5+-247f5bf.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.046x slower

# HPT report

- Reliability score: 99.97% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.36x