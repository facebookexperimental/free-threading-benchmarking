# Results vs. 3.12.6

- fork: Yhg1s
- ref: load_const_defer
- machine: linux-x86_64
- commit hash: fcfb942
- commit date: 2025-01-29
- overall geometric mean: 1.076x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 311 ms: 1.18x slower                                              |
| docutils       | 2.64 sec                                               | 2.85 sec: 1.08x slower                                            |
| html5lib       | 63.6 ms                                                | 72.9 ms: 1.15x slower                                             |
| Geometric mean | (ref)                                                  | 1.13x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 590 ms: 1.88x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 254 ms: 1.75x faster                                              |
| async_tree_io              | 1.08 sec                                               | 619 ms: 1.75x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 325 ms: 1.72x faster                                              |
| async_tree_none            | 464 ms                                                 | 293 ms: 1.58x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 361 ms: 1.54x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 561 ms: 1.29x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 594 ms: 1.20x faster                                              |
| async_generators           | 384 ms                                                 | 378 ms: 1.02x faster                                              |
| coroutines                 | 23.9 ms                                                | 24.5 ms: 1.02x slower                                             |
| Geometric mean             | (ref)                                                  | 1.39x faster                                                      |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 80.8 ms                                                | 77.8 ms: 1.04x faster                                             |
| pidigits       | 184 ms                                                 | 224 ms: 1.22x slower                                              |
| nbody          | 89.3 ms                                                | 142 ms: 1.59x slower                                              |
| Geometric mean | (ref)                                                  | 1.23x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.93 ms: 1.08x faster                                             |
| regex_dna      | 168 ms                                                 | 182 ms: 1.09x slower                                              |
| regex_compile  | 142 ms                                                 | 155 ms: 1.09x slower                                              |
| regex_v8       | 20.6 ms                                                | 24.7 ms: 1.20x slower                                             |
| Geometric mean | (ref)                                                  | 1.07x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                              |
| xml_etree_iterparse  | 96.7 ms                                                | 89.4 ms: 1.08x faster                                             |
| xml_etree_generate   | 85.2 ms                                                | 97.7 ms: 1.15x slower                                             |
| tomli_loads          | 2.11 sec                                               | 2.42 sec: 1.15x slower                                            |
| unpickle_pure_python | 221 us                                                 | 257 us: 1.17x slower                                              |
| xml_etree_process    | 59.0 ms                                                | 70.1 ms: 1.19x slower                                             |
| json_loads           | 26.5 us                                                | 31.7 us: 1.19x slower                                             |
| json_dumps           | 10.4 ms                                                | 13.0 ms: 1.25x slower                                             |
| pickle_pure_python   | 308 us                                                 | 386 us: 1.25x slower                                              |
| Geometric mean       | (ref)                                                  | 1.13x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.57 ms: 1.34x slower                                             |
| python_startup         | 9.93 ms                                                | 15.3 ms: 1.54x slower                                             |
| Geometric mean         | (ref)                                                  | 1.43x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 62.5 ms: 1.24x slower                                             |
| genshi_text     | 22.8 ms                                                | 28.6 ms: 1.25x slower                                             |
| django_template | 34.7 ms                                                | 43.5 ms: 1.25x slower                                             |
| mako            | 11.0 ms                                                | 16.1 ms: 1.46x slower                                             |
| Geometric mean  | (ref)                                                  | 1.30x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 590 ms: 1.88x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 254 ms: 1.75x faster                                              |
| async_tree_io              | 1.08 sec                                               | 619 ms: 1.75x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 325 ms: 1.72x faster                                              |
| async_tree_none            | 464 ms                                                 | 293 ms: 1.58x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 361 ms: 1.54x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 561 ms: 1.29x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 594 ms: 1.20x faster                                              |
| pathlib                    | 21.5 ms                                                | 19.0 ms: 1.13x faster                                             |
| deepcopy                   | 352 us                                                 | 319 us: 1.10x faster                                              |
| gc_traversal               | 3.46 ms                                                | 3.15 ms: 1.10x faster                                             |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                              |
| regex_effbot               | 3.17 ms                                                | 2.93 ms: 1.08x faster                                             |
| xml_etree_iterparse        | 96.7 ms                                                | 89.4 ms: 1.08x faster                                             |
| sqlite_synth               | 2.20 us                                                | 2.08 us: 1.06x faster                                             |
| float                      | 80.8 ms                                                | 77.8 ms: 1.04x faster                                             |
| deepcopy_memo              | 40.3 us                                                | 39.1 us: 1.03x faster                                             |
| async_generators           | 384 ms                                                 | 378 ms: 1.02x faster                                              |
| bpe_tokeniser              | 4.74 sec                                               | 4.69 sec: 1.01x faster                                            |
| coroutines                 | 23.9 ms                                                | 24.5 ms: 1.02x slower                                             |
| go                         | 139 ms                                                 | 142 ms: 1.02x slower                                              |
| comprehensions             | 19.8 us                                                | 20.4 us: 1.03x slower                                             |
| generators                 | 32.2 ms                                                | 33.3 ms: 1.03x slower                                             |
| pycparser                  | 1.17 sec                                               | 1.21 sec: 1.03x slower                                            |
| dulwich_log                | 78.9 ms                                                | 83.4 ms: 1.06x slower                                             |
| deepcopy_reduce            | 3.08 us                                                | 3.25 us: 1.06x slower                                             |
| json                       | 5.02 ms                                                | 5.39 ms: 1.07x slower                                             |
| scimark_sor                | 130 ms                                                 | 140 ms: 1.08x slower                                              |
| docutils                   | 2.64 sec                                               | 2.85 sec: 1.08x slower                                            |
| regex_dna                  | 168 ms                                                 | 182 ms: 1.09x slower                                              |
| regex_compile              | 142 ms                                                 | 155 ms: 1.09x slower                                              |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.4 ms: 1.12x slower                                             |
| pprint_safe_repr           | 743 ms                                                 | 833 ms: 1.12x slower                                              |
| raytrace                   | 299 ms                                                 | 337 ms: 1.13x slower                                              |
| logging_simple             | 6.63 us                                                | 7.47 us: 1.13x slower                                             |
| sqlalchemy_declarative     | 143 ms                                                 | 161 ms: 1.13x slower                                              |
| logging_silent             | 109 ns                                                 | 123 ns: 1.13x slower                                              |
| chaos                      | 62.8 ms                                                | 71.1 ms: 1.13x slower                                             |
| pprint_pformat             | 1.52 sec                                               | 1.73 sec: 1.14x slower                                            |
| sympy_sum                  | 166 ms                                                 | 189 ms: 1.14x slower                                              |
| logging_format             | 7.35 us                                                | 8.42 us: 1.15x slower                                             |
| xml_etree_generate         | 85.2 ms                                                | 97.7 ms: 1.15x slower                                             |
| html5lib                   | 63.6 ms                                                | 72.9 ms: 1.15x slower                                             |
| tomli_loads                | 2.11 sec                                               | 2.42 sec: 1.15x slower                                            |
| sqlglot_normalize          | 107 ms                                                 | 123 ms: 1.15x slower                                              |
| mdp                        | 2.42 sec                                               | 2.79 sec: 1.16x slower                                            |
| pyflate                    | 448 ms                                                 | 518 ms: 1.16x slower                                              |
| thrift                     | 791 us                                                 | 918 us: 1.16x slower                                              |
| crypto_pyaes               | 76.6 ms                                                | 89.1 ms: 1.16x slower                                             |
| scimark_fft                | 342 ms                                                 | 398 ms: 1.17x slower                                              |
| unpickle_pure_python       | 221 us                                                 | 257 us: 1.17x slower                                              |
| sqlglot_optimize           | 53.3 ms                                                | 62.4 ms: 1.17x slower                                             |
| sqlglot_transpile          | 1.67 ms                                                | 1.96 ms: 1.17x slower                                             |
| sympy_str                  | 292 ms                                                 | 342 ms: 1.17x slower                                              |
| 2to3                       | 264 ms                                                 | 311 ms: 1.18x slower                                              |
| xml_etree_process          | 59.0 ms                                                | 70.1 ms: 1.19x slower                                             |
| json_loads                 | 26.5 us                                                | 31.7 us: 1.19x slower                                             |
| regex_v8                   | 20.6 ms                                                | 24.7 ms: 1.20x slower                                             |
| sympy_integrate            | 20.5 ms                                                | 24.6 ms: 1.20x slower                                             |
| sympy_expand               | 468 ms                                                 | 561 ms: 1.20x slower                                              |
| sqlglot_parse              | 1.36 ms                                                | 1.63 ms: 1.20x slower                                             |
| nqueens                    | 80.1 ms                                                | 96.6 ms: 1.21x slower                                             |
| pidigits                   | 184 ms                                                 | 224 ms: 1.22x slower                                              |
| hexiom                     | 6.17 ms                                                | 7.56 ms: 1.23x slower                                             |
| scimark_lu                 | 114 ms                                                 | 140 ms: 1.23x slower                                              |
| scimark_monte_carlo        | 68.4 ms                                                | 84.3 ms: 1.23x slower                                             |
| create_gc_cycles           | 1.09 ms                                                | 1.35 ms: 1.23x slower                                             |
| genshi_xml                 | 50.2 ms                                                | 62.5 ms: 1.24x slower                                             |
| typing_runtime_protocols   | 163 us                                                 | 203 us: 1.25x slower                                              |
| json_dumps                 | 10.4 ms                                                | 13.0 ms: 1.25x slower                                             |
| genshi_text                | 22.8 ms                                                | 28.6 ms: 1.25x slower                                             |
| pickle_pure_python         | 308 us                                                 | 386 us: 1.25x slower                                              |
| django_template            | 34.7 ms                                                | 43.5 ms: 1.25x slower                                             |
| richards                   | 45.9 ms                                                | 57.9 ms: 1.26x slower                                             |
| meteor_contest             | 104 ms                                                 | 131 ms: 1.26x slower                                              |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.74 ms: 1.31x slower                                             |
| richards_super             | 51.9 ms                                                | 67.8 ms: 1.31x slower                                             |
| telco                      | 6.53 ms                                                | 8.58 ms: 1.31x slower                                             |
| fannkuch                   | 372 ms                                                 | 490 ms: 1.32x slower                                              |
| python_startup_no_site     | 7.16 ms                                                | 9.57 ms: 1.34x slower                                             |
| coverage                   | 71.4 ms                                                | 97.8 ms: 1.37x slower                                             |
| deltablue                  | 3.45 ms                                                | 4.76 ms: 1.38x slower                                             |
| mako                       | 11.0 ms                                                | 16.1 ms: 1.46x slower                                             |
| python_startup             | 9.93 ms                                                | 15.3 ms: 1.54x slower                                             |
| nbody                      | 89.3 ms                                                | 142 ms: 1.59x slower                                              |
| bench_thread_pool          | 941 us                                                 | 3.32 ms: 3.53x slower                                             |
| bench_mp_pool              | 10.8 ms                                                | 94.6 ms: 8.76x slower                                             |
| Geometric mean             | (ref)                                                  | 1.12x slower                                                      |

Benchmark hidden because not significant (3): asyncio_websockets, spectral_norm, pylint
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250129-3.14.0a4+-fcfb942-NOGIL/bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.076x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.36x