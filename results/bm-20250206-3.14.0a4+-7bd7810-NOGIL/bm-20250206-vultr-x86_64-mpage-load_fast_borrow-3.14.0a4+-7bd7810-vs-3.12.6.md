# Results vs. 3.12.6

- fork: mpage
- ref: load_fast_borrow
- machine: linux-x86_64
- commit hash: 7bd7810
- commit date: 2025-02-06
- overall geometric mean: 1.039x slower
- HPT reliability: 99.94%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-7bd7810 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 304 ms: 1.15x slower                                              |
| docutils       | 2.64 sec                                               | 2.82 sec: 1.07x slower                                            |
| html5lib       | 63.6 ms                                                | 72.2 ms: 1.13x slower                                             |
| Geometric mean | (ref)                                                  | 1.12x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-7bd7810 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 560 ms: 1.98x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 241 ms: 1.85x faster                                              |
| async_tree_io              | 1.08 sec                                               | 592 ms: 1.83x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 310 ms: 1.81x faster                                              |
| async_tree_none            | 464 ms                                                 | 281 ms: 1.65x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 345 ms: 1.61x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 498 ms: 1.45x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 531 ms: 1.35x faster                                              |
| coroutines                 | 23.9 ms                                                | 22.7 ms: 1.05x faster                                             |
| async_generators           | 384 ms                                                 | 373 ms: 1.03x faster                                              |
| Geometric mean             | (ref)                                                  | 1.47x faster                                                      |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-7bd7810 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 80.8 ms                                                | 72.5 ms: 1.11x faster                                             |
| pidigits       | 184 ms                                                 | 207 ms: 1.12x slower                                              |
| nbody          | 89.3 ms                                                | 131 ms: 1.47x slower                                              |
| Geometric mean | (ref)                                                  | 1.14x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-7bd7810 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.75 ms: 1.15x faster                                             |
| regex_compile  | 142 ms                                                 | 152 ms: 1.07x slower                                              |
| regex_dna      | 168 ms                                                 | 180 ms: 1.07x slower                                              |
| regex_v8       | 20.6 ms                                                | 23.3 ms: 1.13x slower                                             |
| Geometric mean | (ref)                                                  | 1.03x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-7bd7810 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.0 ms: 1.10x faster                                             |
| xml_etree_parse      | 139 ms                                                 | 127 ms: 1.09x faster                                              |
| unpickle_pure_python | 221 us                                                 | 243 us: 1.10x slower                                              |
| tomli_loads          | 2.11 sec                                               | 2.34 sec: 1.11x slower                                            |
| xml_etree_generate   | 85.2 ms                                                | 95.7 ms: 1.12x slower                                             |
| xml_etree_process    | 59.0 ms                                                | 67.7 ms: 1.15x slower                                             |
| pickle_pure_python   | 308 us                                                 | 357 us: 1.16x slower                                              |
| json_loads           | 26.5 us                                                | 31.2 us: 1.18x slower                                             |
| json_dumps           | 10.4 ms                                                | 12.8 ms: 1.24x slower                                             |
| Geometric mean       | (ref)                                                  | 1.09x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-7bd7810 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.79 ms: 1.37x slower                                             |
| python_startup         | 9.93 ms                                                | 15.6 ms: 1.58x slower                                             |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-7bd7810 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.4 ms: 1.18x slower                                             |
| django_template | 34.7 ms                                                | 41.7 ms: 1.20x slower                                             |
| genshi_text     | 22.8 ms                                                | 27.7 ms: 1.21x slower                                             |
| mako            | 11.0 ms                                                | 15.7 ms: 1.43x slower                                             |
| Geometric mean  | (ref)                                                  | 1.25x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-7bd7810 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 1.66 ms: 2.08x faster                                             |
| async_tree_io_tg           | 1.11 sec                                               | 560 ms: 1.98x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 241 ms: 1.85x faster                                              |
| async_tree_io              | 1.08 sec                                               | 592 ms: 1.83x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 310 ms: 1.81x faster                                              |
| async_tree_none            | 464 ms                                                 | 281 ms: 1.65x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 345 ms: 1.61x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 498 ms: 1.45x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 531 ms: 1.35x faster                                              |
| pathlib                    | 21.5 ms                                                | 18.6 ms: 1.16x faster                                             |
| regex_effbot               | 3.17 ms                                                | 2.75 ms: 1.15x faster                                             |
| deepcopy                   | 352 us                                                 | 305 us: 1.15x faster                                              |
| float                      | 80.8 ms                                                | 72.5 ms: 1.11x faster                                             |
| xml_etree_iterparse        | 96.7 ms                                                | 88.0 ms: 1.10x faster                                             |
| sqlite_synth               | 2.20 us                                                | 2.01 us: 1.10x faster                                             |
| xml_etree_parse            | 139 ms                                                 | 127 ms: 1.09x faster                                              |
| deepcopy_memo              | 40.3 us                                                | 37.3 us: 1.08x faster                                             |
| coroutines                 | 23.9 ms                                                | 22.7 ms: 1.05x faster                                             |
| async_generators           | 384 ms                                                 | 373 ms: 1.03x faster                                              |
| logging_silent             | 109 ns                                                 | 106 ns: 1.02x faster                                              |
| bpe_tokeniser              | 4.74 sec                                               | 4.65 sec: 1.02x faster                                            |
| go                         | 139 ms                                                 | 137 ms: 1.02x faster                                              |
| generators                 | 32.2 ms                                                | 31.7 ms: 1.02x faster                                             |
| scimark_sor                | 130 ms                                                 | 128 ms: 1.01x faster                                              |
| deepcopy_reduce            | 3.08 us                                                | 3.15 us: 1.02x slower                                             |
| pycparser                  | 1.17 sec                                               | 1.20 sec: 1.03x slower                                            |
| dulwich_log                | 78.9 ms                                                | 83.3 ms: 1.06x slower                                             |
| raytrace                   | 299 ms                                                 | 316 ms: 1.06x slower                                              |
| json                       | 5.02 ms                                                | 5.34 ms: 1.06x slower                                             |
| regex_compile              | 142 ms                                                 | 152 ms: 1.07x slower                                              |
| docutils                   | 2.64 sec                                               | 2.82 sec: 1.07x slower                                            |
| regex_dna                  | 168 ms                                                 | 180 ms: 1.07x slower                                              |
| chaos                      | 62.8 ms                                                | 67.6 ms: 1.08x slower                                             |
| pyflate                    | 448 ms                                                 | 483 ms: 1.08x slower                                              |
| pprint_safe_repr           | 743 ms                                                 | 801 ms: 1.08x slower                                              |
| pprint_pformat             | 1.52 sec                                               | 1.66 sec: 1.09x slower                                            |
| unpickle_pure_python       | 221 us                                                 | 243 us: 1.10x slower                                              |
| logging_simple             | 6.63 us                                                | 7.32 us: 1.10x slower                                             |
| sqlglot_normalize          | 107 ms                                                 | 118 ms: 1.10x slower                                              |
| mdp                        | 2.42 sec                                               | 2.68 sec: 1.11x slower                                            |
| sqlalchemy_declarative     | 143 ms                                                 | 159 ms: 1.11x slower                                              |
| tomli_loads                | 2.11 sec                                               | 2.34 sec: 1.11x slower                                            |
| sqlglot_transpile          | 1.67 ms                                                | 1.86 ms: 1.11x slower                                             |
| xml_etree_generate         | 85.2 ms                                                | 95.7 ms: 1.12x slower                                             |
| pidigits                   | 184 ms                                                 | 207 ms: 1.12x slower                                              |
| sympy_sum                  | 166 ms                                                 | 187 ms: 1.13x slower                                              |
| thrift                     | 791 us                                                 | 893 us: 1.13x slower                                              |
| regex_v8                   | 20.6 ms                                                | 23.3 ms: 1.13x slower                                             |
| scimark_fft                | 342 ms                                                 | 387 ms: 1.13x slower                                              |
| logging_format             | 7.35 us                                                | 8.32 us: 1.13x slower                                             |
| sqlglot_parse              | 1.36 ms                                                | 1.53 ms: 1.13x slower                                             |
| html5lib                   | 63.6 ms                                                | 72.2 ms: 1.13x slower                                             |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.8 ms: 1.14x slower                                             |
| sqlglot_optimize           | 53.3 ms                                                | 60.7 ms: 1.14x slower                                             |
| crypto_pyaes               | 76.6 ms                                                | 87.9 ms: 1.15x slower                                             |
| xml_etree_process          | 59.0 ms                                                | 67.7 ms: 1.15x slower                                             |
| 2to3                       | 264 ms                                                 | 304 ms: 1.15x slower                                              |
| sympy_str                  | 292 ms                                                 | 337 ms: 1.16x slower                                              |
| pickle_pure_python         | 308 us                                                 | 357 us: 1.16x slower                                              |
| json_loads                 | 26.5 us                                                | 31.2 us: 1.18x slower                                             |
| sympy_integrate            | 20.5 ms                                                | 24.2 ms: 1.18x slower                                             |
| sympy_expand               | 468 ms                                                 | 551 ms: 1.18x slower                                              |
| scimark_lu                 | 114 ms                                                 | 135 ms: 1.18x slower                                              |
| genshi_xml                 | 50.2 ms                                                | 59.4 ms: 1.18x slower                                             |
| hexiom                     | 6.17 ms                                                | 7.34 ms: 1.19x slower                                             |
| nqueens                    | 80.1 ms                                                | 95.6 ms: 1.19x slower                                             |
| typing_runtime_protocols   | 163 us                                                 | 196 us: 1.20x slower                                              |
| django_template            | 34.7 ms                                                | 41.7 ms: 1.20x slower                                             |
| richards                   | 45.9 ms                                                | 55.3 ms: 1.20x slower                                             |
| scimark_monte_carlo        | 68.4 ms                                                | 82.7 ms: 1.21x slower                                             |
| genshi_text                | 22.8 ms                                                | 27.7 ms: 1.21x slower                                             |
| json_dumps                 | 10.4 ms                                                | 12.8 ms: 1.24x slower                                             |
| meteor_contest             | 104 ms                                                 | 129 ms: 1.24x slower                                              |
| richards_super             | 51.9 ms                                                | 64.5 ms: 1.24x slower                                             |
| create_gc_cycles           | 1.09 ms                                                | 1.38 ms: 1.27x slower                                             |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.73 ms: 1.30x slower                                             |
| fannkuch                   | 372 ms                                                 | 489 ms: 1.31x slower                                              |
| telco                      | 6.53 ms                                                | 8.57 ms: 1.31x slower                                             |
| coverage                   | 71.4 ms                                                | 94.7 ms: 1.33x slower                                             |
| deltablue                  | 3.45 ms                                                | 4.59 ms: 1.33x slower                                             |
| python_startup_no_site     | 7.16 ms                                                | 9.79 ms: 1.37x slower                                             |
| mako                       | 11.0 ms                                                | 15.7 ms: 1.43x slower                                             |
| nbody                      | 89.3 ms                                                | 131 ms: 1.47x slower                                              |
| python_startup             | 9.93 ms                                                | 15.6 ms: 1.58x slower                                             |
| bench_thread_pool          | 941 us                                                 | 3.28 ms: 3.48x slower                                             |
| bench_mp_pool              | 10.8 ms                                                | 95.5 ms: 8.85x slower                                             |
| Geometric mean             | (ref)                                                  | 1.08x slower                                                      |

Benchmark hidden because not significant (4): comprehensions, spectral_norm, pylint, asyncio_websockets
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250206-3.14.0a4+-7bd7810-NOGIL/bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-7bd7810.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.039x slower

# HPT report

- Reliability score: 99.94% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.36x